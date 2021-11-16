# successful install of TA-Lib on M1 mac

[Followed these instructions](https://stackoverflow.com/questions/64963370/error-cannot-install-in-homebrew-on-arm-processor-in-intel-default-prefix-usr/64997047#64997047)

> Homebrew needs to be installed in two places on Apple silicon: in /usr/local for rosetta-emulated (Intel) code, and /opt/homebrew for ARM64. These are somewhat hard-coded and the /opt/homebrew one MUST be used for ARM code, as it stands today, and is non-negotiable. However, it's easy enough to install and you can follow the general instructions on the official docs. You open a Rosetta shell first.

```
cd /usr/local && mkdir homebrew
curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
/opt/homebrew/bin/brew install sometool
brew reinstall ta-lib
pip3 install numpy
pip3 install ta-lib
```