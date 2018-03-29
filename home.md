<!-- TITLE: Home -->
<!-- SUBTITLE: A quick summary of Home -->

# Header
* *Hello* **see** lkappel.free.fr

```perl

sub eee {
    my ($hash_ref, $hash_defines_ref) = @_;
    my %hash_defines = %${hash_defines_ref};
    my %hash = %${hash_ref};
    my %hash0;

    foreach my $k (keys (%hash)) {

        my $hash2_ref = $hash{$k};
        my %hash2 = %${hash2_ref};
        foreach my $k2 (keys (%hash2)) {
            my $hash3_ref = $hash2{$k2}{h};
            my %hash3 = %${hash3_ref};
            foreach my $k3 (keys (%hash3)) {
                my $hash4_ref = $hash3{$k3};
                my %hash4 = %${hash4_ref};

                my $id=$hash4{id};

                my $translate;
                if (exists $hash_defines{$id}) {
                    $translate=$hash_defines{$id};
                } else {
                    $translate="'no defined'";
                }

                $hash0{$k}{$k2}{h}{$k3}=$translate;
                $hash0{$k}{$k2}{a}=$hash2{$k2}{a};
            }

        }
    }

    return %hash0;
}

```
