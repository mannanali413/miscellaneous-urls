# Node Versioning

A brief to Understanding ~, ^ 

## Tilde Ranges ~1.2.3 ~1.2 ~1
- Allows patch-level changes if a minor version is specified on the comparator.  	Allows minor-level changes if not.
E.g. 
* ~1.2.3 := >=1.2.3 <1.(2+1).0 := >=1.2.3 <1.3.0
* ~1.2 := >=1.2.0 <1.(2+1).0 := >=1.2.0 <1.3.0 (Same as 1.2.x)
* ~1 := >=1.0.0 <(1+1).0.0 := >=1.0.0 <2.0.0 (Same as 1.x)

## Caret Ranges ^1.2.3 ^0.2.5 ^0.0.4
- Allows changes that do not modify the left-most non-zero digit in the [major, minor, patch] tuple. In other words, this allows patch and minor updates for versions 1.0.0 and above, patch updates for versions 0.X >=0.1.0, and noupdates for versions 0.0.X.
E.g.
* ^1.2.3 := >=1.2.3 <2.0.0
* ^0.2.3 := >=0.2.3 <0.3.0
* ^0.0.3 := >=0.0.3 <0.0.4
* ^1.2.x := >=1.2.0 <2.0.0
* ^0.0.x := >=0.0.0 <0.1.0
* ^0.0 := >=0.0.0 <0.1.0
