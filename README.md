# temp-spock
A simple stub project to help a redditor compile Spock on Windows. See: http://www.reddit.com/r/haskell/comments/332s1k/what_haskell_web_framework_do_you_use_and_why/cqjacvx

`$` indicates a command prompt. It was a normal Windows prompt, I just renamed it for cleaner git README formatting. I've also made some inline replacements, for privacy.

Running from a command prompt on Windows 8.1 using Haskell Platform 2014.2.0.0:

> mkdir temp-spock

> cd temp-spock

> $ ghc --version
```
The Glorious Glasgow Haskell Compilation System, version 7.8.3
```

> $ cabal --version
```
cabal-install version 1.20.0.3
using version 1.20.0.2 of the Cabal library
```

> $ cabal sandbox init
```
Writing a default package environment file to
...\temp-spock\cabal.sandbox.config
Creating a new sandbox at
...\temp-spock\.cabal-sandbox
```

> $ cabal update
```
Downloading the latest package list from hackage.haskell.org
Note: there is a new version of cabal-install available.
To upgrade, run: cabal install cabal-install
```

> $ cabal init
```
Package name? [default: temp-spock]
Package version? [default: 0.1.0.0]
Please choose a license:
 * 1) (none)
   2) GPL-2
   3) GPL-3
   4) LGPL-2.1
   5) LGPL-3
   6) AGPL-3
   7) BSD2
   8) BSD3
   9) MIT
  10) MPL-2.0
  11) Apache-2.0
  12) PublicDomain
  13) AllRightsReserved
  14) Other (specify)
Your choice? [default: (none)]
Author name? [default: xxx]
Maintainer email? [default: xxx@gmail.com]
Project homepage URL?
Project synopsis?
Project category:
 * 1) (none)
   2) Codec
   3) Concurrency
   4) Control
   5) Data
   6) Database
   7) Development
   8) Distribution
   9) Game
  10) Graphics
  11) Language
  12) Math
  13) Network
  14) Sound
  15) System
  16) Testing
  17) Text
  18) Web
  19) Other (specify)
Your choice? [default: (none)]
What does the package build:
   1) Library
   2) Executable
Your choice? 1
What base language is the package written in:
 * 1) Haskell2010
   2) Haskell98
   3) Other (specify)
Your choice? [default: Haskell2010]
Include documentation on what each field means (y/n)? [default: n]
Guessing dependencies...
Generating LICENSE...
Warning: unknown license type, you must put a copy in LICENSE yourself.
Generating Setup.hs...
Generating temp-spock.cabal...
Warning: no synopsis given. You should edit the .cabal file and add one.
You may want to edit the .cabal file and add a Description field.
```

> $ ... (Created SpockTest.hs + defined it as an exposed-module and added a build-depends for Spock to temp-spock.cabal... See the two other files in this git repo.)

> $ cabal configure
```
Resolving dependencies...
Configuring temp-spock-0.1.0.0...
cabal: At least the following dependencies are missing:
Spock -any
```

> $ cabal install Spock
```
Resolving dependencies...
Notice: installing into a sandbox located at
...\temp-spock\.cabal-sandbox
Configuring appar-0.1.4...
Configuring ansi-terminal-0.6.2.1...
Configuring auto-update-0.1.2.1...
Downloading transformers-compat-0.4.0.3...
Configuring base64-bytestring-1.0.0.1...
Building appar-0.1.4...
Building auto-update-0.1.2.1...
Building base64-bytestring-1.0.0.1...
Building ansi-terminal-0.6.2.1...
Configuring byteorder-1.0.4...
Installed auto-update-0.1.2.1
Installed appar-0.1.4
Building byteorder-1.0.4...
Configuring blaze-builder-0.4.0.1...
Configuring bytestring-builder-0.10.6.0.0...
Installed base64-bytestring-1.0.0.1
Installed ansi-terminal-0.6.2.1
Configuring data-default-class-0.0.1...
Configuring dlist-0.7.1.1...
Installed byteorder-1.0.4
Building bytestring-builder-0.10.6.0.0...
Building blaze-builder-0.4.0.1...
Building data-default-class-0.0.1...
Configuring easy-file-0.2.0...
Building dlist-0.7.1.1...
Installed bytestring-builder-0.10.6.0.0
Configuring mmorph-1.0.4...
Installed data-default-class-0.0.1
Building easy-file-0.2.0...
Configuring nats-1...
Installed dlist-0.7.1.1
Building mmorph-1.0.4...
Configuring path-pieces-0.2.0...
Installed blaze-builder-0.4.0.1
Downloading streaming-commons-0.1.12...
Building nats-1...
Installed easy-file-0.2.0
Configuring safe-0.3.8...
Building path-pieces-0.2.0...
Configuring scientific-0.2.0.2...
Installed mmorph-1.0.4
Configuring stringsearch-0.3.6.6...
Installed nats-1
Building safe-0.3.8...
Building scientific-0.2.0.2...
Configuring unix-compat-0.4.1.4...
Installed path-pieces-0.2.0
Building stringsearch-0.3.6.6...
Configuring vault-0.3.0.4...
Installed safe-0.3.8
Downloading graph-core-0.2.2.0...
Building unix-compat-0.4.1.4...
Building vault-0.3.0.4...
Installed scientific-0.2.0.2
Configuring word8-0.1.2...
Building word8-0.1.2...
Configuring transformers-compat-0.4.0.3...
Installed vault-0.3.0.4
Installed word8-0.1.2
Configuring iproute-1.4.0...
Building transformers-compat-0.4.0.3...
Configuring fast-logger-2.3.1...
Installed unix-compat-0.4.1.4
Configuring data-default-instances-base-0.0.1...
Building iproute-1.4.0...
Installed stringsearch-0.3.6.6
Building fast-logger-2.3.1...
Building data-default-instances-base-0.0.1...
Configuring data-default-instances-containers-0.0.1...
Installed fast-logger-2.3.1
Configuring data-default-instances-old-locale-0.0.1...
Installed transformers-compat-0.4.0.3
Building data-default-instances-containers-0.0.1...
Configuring data-default-instances-dlist-0.0.1...
Installed data-default-instances-base-0.0.1
Building data-default-instances-old-locale-0.0.1...
Installed iproute-1.4.0
Configuring http-types-0.8.6...
Building data-default-instances-dlist-0.0.1...
Configuring streaming-commons-0.1.12...
Installed data-default-instances-containers-0.0.1
Configuring semigroups-0.16.2.2...
Installed data-default-instances-old-locale-0.0.1
Building http-types-0.8.6...
Configuring graph-core-0.2.2.0...
Installed data-default-instances-dlist-0.0.1
Building streaming-commons-0.1.12...
Building semigroups-0.16.2.2...
Building graph-core-0.2.2.0...
Configuring aeson-0.7.0.4...
Installed http-types-0.8.6
Building aeson-0.7.0.4...
Installed graph-core-0.2.2.0
Downloading reroute-0.2.2.1...
Configuring exceptions-0.8.0.2...
Building exceptions-0.8.0.2...
Configuring transformers-base-0.4.4...
Installed streaming-commons-0.1.12
Configuring data-default-0.5.3...
Installed semigroups-0.16.2.2
Building transformers-base-0.4.4...
Installed exceptions-0.8.0.2
Configuring wai-3.0.2.3...
Building data-default-0.5.3...
Installed data-default-0.5.3
Configuring reroute-0.2.2.1...
Building wai-3.0.2.3...
Configuring void-0.7...
Installed transformers-base-0.4.4
Building reroute-0.2.2.1...
Configuring cookie-0.4.1.4...
Installed wai-3.0.2.3
Building void-0.7...
Building cookie-0.4.1.4...
Installed void-0.7
Configuring monad-control-1.0.0.4...
Configuring wai-logger-2.2.4...
Installed cookie-0.4.1.4
Building monad-control-1.0.0.4...
Installed reroute-0.2.2.1
Building wai-logger-2.2.4...
Installed monad-control-1.0.0.4
Configuring resource-pool-0.2.3.2...
Configuring lifted-base-0.2.3.6...
Configuring resourcet-1.1.4.1...
Building resourcet-1.1.4.1...
Installed resourcet-1.1.4.1
Downloading wai-extra-3.0.7...
Configuring conduit-1.2.4...
Configuring wai-extra-3.0.7...
Building conduit-1.2.4...
Building wai-extra-3.0.7...
Installed conduit-1.2.4
Downloading conduit-extra-1.1.7.2...
Configuring conduit-extra-1.1.7.2...
Building conduit-extra-1.1.7.2...
Installed wai-extra-3.0.7
Installed conduit-extra-1.1.7.2
Configuring simple-sendfile-0.2.18...
Building simple-sendfile-0.2.18...
Installed simple-sendfile-0.2.18
Downloading warp-3.0.12...
Configuring warp-3.0.12...
Building warp-3.0.12...
Installed warp-3.0.12
Downloading Spock-0.7.9.0...
Configuring Spock-0.7.9.0...
Building Spock-0.7.9.0...
Installed Spock-0.7.9.0
```

# Done!
