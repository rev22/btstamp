Notarize a file into the bitcoin blockchain, command-line version.

[Trusted digital timestamping](http://en.wikipedia.org/wiki/Trusted_timestamping) can be used to certify that you held a certain information at a certain point in time.

### Usage

First run btstamp on your file.  Btstamp hashes your file into a bitcoin address.

```
$ ./btstamp poem.txt
12c3xdrDuoHBz8R6zo8kWJXtnTmBNx8cbA
```

Then transfer a fractional amount of bitcoins to the generated address.  This destroys the bitcoins, so just send a minimal amount.

After the transfer was accepted by the bitcoin network, you can use a blockchain viewer to verify the transaction date.  Be sure to keep an exact copy of the hashed data or this proof won't be valid.

This software uses [btproof](https://www.btproof.com/)'s algorithm and code, and is indeed compatible with btproof.

### Install

The btstamp script requires btproof's website sources, which you can obtain by importing the 'btproof' submodule.

```
git submodule init
git submodule update
```

### Authors and licensing

The "btstamp" script was created by Michele Bini and is available with a MIT-style license.  Please consult the LICENSE file for more information.

It links to "btproof" code that is also available with a MIT-style license. (https://github.com/shesek/btproof)