# msstats

Calculates summary stats from Hudson's ms. Includes two programs:

	msstats - read data from ms via stdin, calculate common summary statistics
	mssfs - read data from ms via stdin, calculate the unfolded site frequency spectrum

## Installation

I find on Unix systems, the following is often necessary:

PPFLAGS=-I$LIBSEQUENCE/include LDFLAGS=-L$LIBSEQUENCE/lib ./configure 

where $LIBSEQUENCE is the directory into which [libsequence](https://github.com/RILAB/libsequence) has been installed. 

## Original Copyright distributed with msstats 0.3.2

  Copyright (C) 2002 Kevin Thornton

  msstats is free software; you can redistribute it and/or modify
  it under the terms of the GNU General Public License as published by
  the Free Software Foundation; either version 2 of the License, or
  (at your option) any later version.

  This program is distributed in the hope that it will be useful,
  but WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
  GNU General Public License for more details.

  You should have received a copy of the GNU General Public License
  along with this program; if not, write to the Free Software
  Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA

Comments are welcome.

	- Kevin Thornton <k-thornton@uchicago.edu>
