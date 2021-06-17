tlsrestrictchromium
===================

tlsrestrictchromium was a tool for blacklisting all built-in TLS CA's for a specific eTLD.  It was previously used by Namecoin.  As tlsrestrictchromium requires HPKP, which has since been removed by Chromium, tlsrestrictchromium               is obsolete.

Building
--------

Prerequisites:

1. Ensure you have the Go tools installed.

Option A: Using Go build commands without Go modules (works on any platform with Bash; only Go 1.15-1.16.x; will not work on Go 1.17+):

1. Ensure you have the `GOPATH` environment variable set. (For those not
   familar with Go, setting it to the path to an empty directory will suffice.
   The directory will be filled with build files.)

2. Run `export GO111MODULE=off` to disable Go modules.

3. Run `go get -t -u github.com/namecoin/tlsrestrictchromium/...`.  tlsrestrictchromium will be built. The binaries will be at `$GOPATH/bin/tlsrestrictchromium`.

Option B: Using Go build commands with Go modules (works on any platform with Bash; Go 1.15+:

1. Run the following in the tlsrestrictchromium directory to set up Go modules:
   
   ~~~
   go mod init
   go mod tidy
   ~~~

2. Run `go install ./...`.  tlsrestrictchromium will be built. The binaries will be at `$GOPATH/bin/tlsrestrictchromium`.

Option C: Using Makefile (non-Windows platforms):

1. Run `make`. The source repository will be retrieved via `go get`
   automatically.

Licence
-------
    Licenced under the GPLv3 or later.
    © 2014-2015 Hugo Landau <hlandau@devever.net>
