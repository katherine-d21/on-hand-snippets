**Handy Regex**

* To remove human, decoys, and contaminants (case-insensitive)

 >  NOT Matching (\t(generic\|)?((?i)con_|contam_|rev_|decoy_)|((?i)_human\t))

Explanation:
Match, any case upper or lower, a line a column that starts with `con_`, `contam_`, `rev_`, `decoy_`, with an optional `generic|` in front, or a column that ends with `_human`.
using the `\t` tab here to delineated where a column starts or ends because it's tab-separated values.

* To obtain human lines (no overlap with contaminants/decoys)
    * First, select human proteins
    > Matching (?i)_human\t
    * Then, remove contaminants/decoys
    > NOT matching \t(generic\|)?((?i)con_|contam_|rev_|decoy_)
