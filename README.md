<img height=40 src='http://my5C.umassmed.edu/images/3DG.png' title='3D-Genome' />
&nbsp;&nbsp;
<img height=30 src='http://my5C.umassmed.edu/images/dekkerlabbioinformatics.gif' />
&nbsp;&nbsp;
<img height=30 src='http://my5C.umassmed.edu/images/umasslogo.gif' />

# balance

balance hdf5 hi-c matrix [sinkhorn knopp]

```
scripts/
	balance.py - balance hdf5 hi-c matrix [sinkhorn knopp]
```

## Installation

The main requirements are numpy and h5py.

You can install the dependencies with

for req in $(cat requirements.txt); do pip install $req; done

## Full Documentation

## Communication

- [Bryan Lajoie](https://github.com/blajoie)
- [Noam Kaplan](https://github.com/NoamKaplan)
- Twitter: [@my5C](https://twitter.com/my5C)

## What does it do?

balance performs a sinkhorn-knopp iterative correction to a hi-c interaction matrix

## Usage

```

usage : $ python scripts/balance.py --help

usage: balance.py [-h] -in INFILE [-out OUTFILE] [-or] [-f FACTORFILE]
                  [-b BLOCKSIZE] [-t THRESHOLD] [-s MINIMAL_SUM]
                  [-ddt DELTA_DELTA_LIMIT] [-etl ELAPSED_TIME_LIMIT]
                  [-mi MAX_ITERATIONS] [-nan NAN_VAL] [-d]

Apply Sinkhorn Balancing to interaction matrix.

optional arguments:
  -h, --help            show this help message and exit
  -in INFILE            interaction matrix hdf5 file (default: None)
  -out OUTFILE          output hdf5 file (default: None)
  -or, --output_relative
                        output file relative to input file path (default:
                        False)
  -f FACTORFILE         output factor file (default: None)
  -b BLOCKSIZE          block size (default: hdf chunk size) (default: None)
  -t THRESHOLD          balancing threshold (default: 1e-05)
  -s MINIMAL_SUM        minimal sum threshold (default: 1e-05)
  -ddt DELTA_DELTA_LIMIT
                        deltadelta threshold (default: 1e-06)
  -etl ELAPSED_TIME_LIMIT
                        elapsed time limit (default: 129600)
  -mi MAX_ITERATIONS    max iterations (default: 10000)
  -nan NAN_VAL          replace isolated isolated nans with this value
                        (default: import from neighborhood) (default: None)
  -d                    ignore diagonal in factor calculation (default: False)

```

## Usage Examples

## Change Log

## Bugs and Feedback

For bugs, questions and discussions please use the [Github Issues](https://github.com/blajoie/tab2hdf/issues).

## LICENSE

Licensed under the Apache License, Version 2.0 (the 'License');
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

<http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an 'AS IS' BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

