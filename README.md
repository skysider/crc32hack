CRC32 Tools
===========
[![Build Status](https://travis-ci.org/theonlypwner/crc32.svg)](https://travis-ci.org/theonlypwner/crc32)
[![Coverage Status](https://coveralls.io/repos/github/theonlypwner/crc32/badge.svg)](https://coveralls.io/github/theonlypwner/crc32)
[![Code Health](https://landscape.io/github/theonlypwner/crc32/master/landscape.svg?style=flat)](https://landscape.io/github/theonlypwner/crc32/master)

License
-----------
This project is licensed under the GPL v3 license.

Usage
-----------
Run the command line to see usage instructions:
```
crc32.py -h
usage: crc32.py [-h] action ...

Reverse, undo, and calculate CRC32 checksums

positional arguments:
  action
    flip      flip the bits to convert normal(msbit-first) polynomials to
              reversed (lsbit-first) and vice versa
    reciprocal
              find the reciprocal (Koopman notation) of a reversed (lsbit-
              first) polynomial and vice versa
    table     generate a lookup table for a polynomial
    reverse   find a patch that causes the CRC32 checksum to become a desired
              value
    undo      rewind a CRC32 checksum
    calc      calculate the CRC32 checksum

optional arguments:
  -h, --help  show this help message and exit
```

## Example

```python
(pwn) ➜  python crc32.py reverse 0x201472db
4 bytes: {0x66, 0x31, 0x41, 0x67}
verification checksum: 0x201472db (OK)
f1Ag

alternative 5 bytes:

alternative 6 bytes:
alternative: 7gVwIe (OK)
alternative: 9hIGuk (OK)
alternative: Fz8Sk0 (OK)
alternative: QoE35X (OK)
alternative: Y411Ul (OK)
alternative: YeSP9p (OK)
alternative: _18beJ (OK)
alternative: bmY7PB (OK)
alternative: cqWZJO (OK)
alternative: fTUz9y (OK)
alternative: p1UZyX (OK)
alternative: uYzGgf (OK)
    

(pwn) ➜  python crc32.py reverse 0x38f7bcc6
4 bytes: {0xd1, 0x6a, 0xb4, 0x29}
verification checksum: 0x38f7bcc6 (OK)

alternative 5 bytes:
alternative: f1Ag_ (OK)

alternative 6 bytes:
alternative: 5VYNTH (OK)
alternative: AOkZlg (OK)
alternative: CsnD5z (OK)
alternative: FVldFL (OK)
alternative: HYsTzB (OK)
alternative: RBDg2x (OK)
alternative: WgFGAN (OK)
alternative: b11qxn (OK)
alternative: gEQ0gD (OK)
alternative: msBM2q (OK)
alternative: oOGSkl (OK)
alternative: qq3qKy (OK)
alternative: tT1Q8O (OK)
alternative: vh4OaR (OK)
alternative: ygjNFE (OK)
```

