# pthr16LimitedCandTreeSet

RDS files starting with candTrees should be in approximately aphylo form (although it's possible there is something slightly off about them, not clear what issue is but wouldn't generate figures and odd message when doing parameter estimates seemingl)

All annotations were taken which used experimental evidence codes seemingly from the panther 16 set of annotations. Any proteins with both positive and negative annotations for same go term should be removed  

evidence codes used = 'EXP', 'IDA', 'IPI', 'IMP', 'IGI', 'IEP', 'HTP', 'HAD', 'HMP', 'HGI', 'HEP', 'IKR'

horizontal transfer nodes and speciation nodes both labeled as 1s, duplications as 0s
conflicts with non experimental evidence codes were not taken into account here. 
Only is_a relationships were used in this case for the ontology constraints
obsolete go terms were removed from annotations list and alt names should have been updated to standard names 

+o means ontology constraints added
+t means taxon constraints added 
-da means annotations under same branch of a duplication node which conflict were replaced by 9s 
-dt means trees with conflicts under same branch of a duplication node were removed entirely 

original set was 138 trees
candTreesannoonlyall.rds = 127 trees, some trees had no annos any longer and some trees were not part of panther 16
candtreesanno>1pos+neg.rds 67 trees from original set with >1 positive and >1 negative annotation
candTrees+o+t.rds 72 trees with >1pos>1neg with ontology and taxon constraints
candTrees+o+t-da.rds 68 trees same as candTrees+o+t but with conflicting annotations in same branch of duplication node relabeled as 9s
candTrees+o+t-dt.rds 65 trees same as candTrees+o+t with trees with conflicting branches removed entirely 

in this set there were no taxon conflicts with default annotations, there were 3 ontology conflicts with default annotations (relabeled as 9s), no conflicts between taxon and ontology constraints




