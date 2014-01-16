# msstats

Calculates summary stats from Hudson's ms. Includes two programs:

	msstats - read data from ms via stdin, calculate common summary statistics
	mssfs - read data from ms via stdin, calculate the unfolded site frequency spectrum

## Fst functionality

Added to this version is the ability to calculate shared, fixed, and unique polymorphisms in comparisons of two populations. 
This requires using the "-F" flag in addition to the standard "-I npops n1 n2" notation. This currently only works for 2 populations.
Fst is calculated using the libsequence [HBK function](http://molpopgen.org/software/libsequence/doc/html/classSequence_1_1FST.html#a3dc3987daf9d4e4b7f6c39fdba53b68e).
Note that unique polymorphisms are calculated in a perhaps non-intuitive manner:

In the example below (two populations, two individuals, 3 sites), population 1 has 2 unique sites, and population 2 has 1 unique site.
Thus, sites in which one population is fixed for the derived alleles but the other is polymorphic will be counted as unique to one popualtion rather than shared.

	Pop1
	010
	100

	Pop2
	010
	011

For an alternative implementation of Fst in msstats (but not shared, fixed, etc.) you can see [msstatsFST](https://github.com/rossibarra/msstatsFST) which calculates Weir and Cockerham's Fst statistic.

## Installation

I find on Unix systems, the following is often necessary:

	CPPFLAGS=-I$LIBSEQUENCE/include LDFLAGS=-L$LIBSEQUENCE/lib ./configure 

where $LIBSEQUENCE is the directory into which [libsequence](https://github.com/RILAB/libsequence) has been installed. 


## Contact

Please contact [Kevin Thornton](www.molpopgen.org) for questions about the original code, or [Jeff Ross-Ibarra](www.rilab.org) for questions about the modified version or this repo.

