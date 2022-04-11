Thoses are the lokinet packages I've build for my starfive risc-v board.

I've follow the guide of necro-nemesis for the build. (https://github.com/necro-nemesis/Lokinet-RPM-package) 

When you'll clone the oxen-mq (git clone --recursive https://github.com/oxen-io/oxen-mq) and the lokinet github repo (https://github.com/oxen-io/lokinet) don't forget to switch (git switch fedora/33)to fedora 33 branch (and fedora 34 for lokinet, it will work) and to re run "git submodule update init --recursive" If you don't you'll miss packages when you'll try to build oxen-mq and lokinet

You'll also need to install resolvconf (sudo dnf install -y resolvconf)

You'll have to modify the following file in the necro-nemesis repo "./Lokinet-RPM-package/SPECS/lokinet.spec" and remove the line 56 and the line 57 (it's for x86_64 CPU, lokinet won't build if you don't)



