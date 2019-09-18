# RISC-V Software Ecosystem Overview

This document captures the status of the RISC-V Software Ecosystem. Please add
to the list and fix inaccuracies.

* [Simulators](#simulators)
* [Object toolchain](#object-toolchain)
* [Debugging](#debugging)
* [C compilers and libraries](#c-compilers-and-libraries)
* [Boot loaders and monitors](#boot-loaders-and-monitors)
* [OS and OS kernels](#os-and-os-kernels)
* [Compilers and runtimes for other languages](#compilers-and-runtimes-for-other-languages)
* [IDEs](#ides)
* [Security](#security)

**We would like to enlist community help for the software ports in the [Help Wanted](#help-wanted) section.**

# Simulators

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
DBT-RISE-RISCV | [github](https://github.com/Minres/DBT-RISE-RISCV) | BSD-3-Clause | [MINRES Technologies](www.minres.com)
FireSim | [website](https://fires.im), [mailing list](https://groups.google.com/forum/#!forum/firesim), [github](https://github.com/firesim/firesim), [ISCA 2018 Paper](https://sagark.org/assets/pubs/firesim-isca2018.pdf) | BSD | Sagar Karandikar, Howard Mao, Donggyu Kim, David Biancolin, Alon Amid, [Berkeley Architecture Research](https://bar.eecs.berkeley.edu)
gem5 | [SW-dev thread](https://groups.google.com/a/groups.riscv.org/forum/#!topic/sw-dev/se0TVeaA_JI), [repository](https://gem5.googlesource.com/public/gem5/) | BSD-style | Alec Roelke (University of Virginia)
Imperas | [website](http://www.imperas.com/riscv) | Proprietary, models available under Apache 2.0 | [Imperas](http://www.imperas.com/)
riscvOVPsim | [github](https://github.com/riscv/riscv-ovpsim) | [license](https://github.com/riscv/riscv-ovpsim/blob/master/LICENSE.pdf) | [Imperas](http://www.imperas.com/)
OVPsim | [website](http://www.ovpworld.org/riscv) | Free for non commercial use, models available under Apache 2.0 | [Imperas](http://www.imperas.com/)
jor1k | [website](http://s-macke.github.io/jor1k/demos/riscv.html), [github](https://github.com/s-macke/jor1k/) | BSD 2-Clause | Sebastian Macke
Jupiter | [github](https://github.com/andrescv/Jupiter) | GPL-3.0 | Andrés Castellanos
MARSS-RISCV | [github](https://github.com/bucaps/marss-riscv) | MIT | Gaurav N Kothari, Parikshit P Sarnaik, Gokturk Yuksek (State University of New York at Binghamton)
QEMU | [upstream](http://git.qemu.org/qemu.git) | GPL | Sagar Karandikar (University of California, Berkeley), Bastian Koppelmann (University of Paderborn), Alex Suykov, Stefan O'Rear and Michael Clark (SiFive)
RARS | [github](https://github.com/thethirdone/rars) | MIT | Benjamin Landers
Renode | [website](https://renode.io), [github](https://github.com/renode/renode) | MIT | [Antmicro](https://antmicro.com)
Ripes | [github](https://github.com/mortbopet/Ripes)| MIT | Morten Borup Petersen
RISC-V Virtual Prototype | [website](http://www.systemc-verification.org/riscv-vp), [github](https://github.com/agra-uni-bremen/riscv-vp) | MIT | Vladimir Herdt (University of Bremen, [AGRA](http://www.informatik.uni-bremen.de/agra/eng/index.php))
TinyEMU | [website](http://bellard.org/riscvemu/) | MIT | Fabrice Bellard
Spike | [github](https://github.com/riscv/riscv-isa-sim) | BSD 3-clause | Andrew Waterman & Yunsup Lee (SiFive)
Swerv-ISS  | [github](https://github.com/westerndigitalcorporation/swerv-ISS) | GPL - 3 | Joseph Rahmeh (Western Digital) 
VLAB  | [VLAB Works](http://vlabworks.com/) | Proprietary | [ASTC](http://astc-design.com/)

# Object toolchain

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
Binutils | [RISC-V repo](https://github.com/riscv/riscv-binutils-gdb), [Upstream repos](https://sourceware.org/git/gitweb.cgi?p=binutils-gdb.git) | GPLv2 | Andrew Waterman, Palmer Dabbelt & Jim Wilson (SiFive)
LLVM | [GitHub mirror](https://github.com/llvm-mirror/llvm/tree/master/lib/Target/RISCV) | Apache 2.0 with LLVM exception | Alex Bradbury (lowRISC)
Cranelift | [GitHub](https://github.com/CraneStation/cranelift) | Apache 2.0 | [Cranelift core team](https://github.com/orgs/CraneStation/people/)

# Debugging


Name | Links | License | Maintainers
---- | ----- | ------- | -----------
GDB | [Upstream](https://sourceware.org/git/gitweb.cgi?p=binutils-gdb.git) | GPLv2 | Andrew Burgess (Embecosm), Palmer Dabbelt (SiFive)
OpenOCD | [Upstream repo](https://sourceforge.net/p/openocd/code/ci/master/tree/), [RISC-V repo](https://github.com/riscv/riscv-openocd) | GPLv2 | Tim Newsome, Megan Wachs, Palmer Dabbelt (SiFive)
GNU MCU Eclipse OpenOCD | [Website](https://gnu-mcu-eclipse.github.io/openocd/), [GitHub](https://github.com/gnu-mcu-eclipse/openocd) | GPLv2 | Liviu Ionescu
Ozone - the J-Link Debugger | [Website](https://www.segger.com/ozone) | SEGGER commercial license (J-Link PLUS) | [SEGGER](https://www.segger.com/)
Imperas Multi Processor Debugger | [Website](http://www.imperas.com/riscv#debug) | Imperas Commercial License | [Imperas](http://www.imperas.com/)
TCF Debugger | [Website](https://projects.eclipse.org/projects/tools.cdt.tcf), [GitHub](https://github.com/eclipse/tcf.agent) | Eclipse Distribution License 1.0 (BSD) / Eclipse Public License 1.0 | Sanimir Agovic

# C compilers and libraries


Name | Links | License | Maintainers
---- | ----- | ------- | -----------
GCC	| [Upstream](https://gcc.gnu.org/viewcvs/gcc/trunk/), [RISC-V repository](https://github.com/riscv/riscv-gcc) | GPLv3	| Andrew Waterman (SiFive), Palmer Dabbelt (SiFive), Jim Wilson (SiFive), Kito Cheng (Andes)
GNU MCU Eclipse RISC-V Embedded GCC (riscv-non-embed-gcc)	| [Web](https://gnu-mcu-eclipse.github.io/toolchain/riscv/), [Repository](https://github.com/gnu-mcu-eclipse/riscv-none-gcc), [Build](https://github.com/gnu-mcu-eclipse/riscv-none-gcc-build), [Binary package installer](https://www.npmjs.com/package/@gnu-mcu-eclipse/riscv-none-gcc)	| Eclipse Public License |	Liviu lonescu
Clang/LLVM	| [Upstream](https://github.com/llvm-mirror/llvm)	| Apache 2.0	| Alex Bradbury (lowRISC)
CompCert	| [Upstream](https://github.com/AbsInt/CompCert.git)	| INRIA Non-Commercial License Agreement	| Xavier Leroy
Glibc	| [Upstream](https://sourceware.org/git/?p=glibc.git), [RISC-V repository](https://github.com/riscv/riscv-glibc) |	GPLv2 |	Palmer Dabbelt (SiFive), Andrew Waterman (SiFive), DJ Delorie (Red Hat), Darius Rad(Bluespec)
Newlib	| [Upstream](http://cygwin.com/git/gitweb.cgi?p=newlib-cygwin.git), [RISC-V repository](https://github.com/riscv/riscv-newlib)	| GPLv2	| Kito Cheng (Andes)
SEGGER Runtime Library | [Website](https://www.segger.com/products/development-tools/runtime-library/) | SEGGER commercial license | [SEGGER](https://www.segger.com/)
Musl	| -	| - | -

# Boot loaders and monitors

## coreboot ##

* Maintainer(s): Ron Minnich (Google), Jonathan Neuschäfer
* Version: master
* Status: runs on spike, lowRISC/Nexys4DDR. Linux doesn't quite work yet.
* Upstreaming status: upstream
* Future work:
* RISC-V repository:
* Upstream repository: https://review.coreboot.org/cgit/coreboot.git/
* Privileged Spec: 1.9
* User Spec: 2.0
* ABI:

More information:
* https://riscv.org/wp-content/uploads/2016/01/Tues1345-riscvcoreboot.pdf
* https://www.youtube.com/watch?v=-KnwZzbvp1c (coreboot on RISC-V, Ron Minnich, RISC-V workshop)
* https://www.youtube.com/watch?v=CDNIWuf1jAk (coreboot on RISC-V, Ron Minnich, coreboot conference 2016)

## UEFI ##

* Maintainer(s): Abner Chang, Dong Wei (HP Enterprise)
* Version:
* Status:
* Upstreaming status:
* Future work:
* RISC-V repository:
* Upstream repository:
* Privileged Spec:
* User Spec: 2.0
* ABI:

https://riscv.org/wp-content/uploads/2016/01/Tues1415-RISC-V-and-UEFI.pdf

## Proxy Kernel/BBL ##

* Maintainer(s):
* Version:
* Status:
* Upstreaming status:
* Future work:
* Upstream repository: https://github.com/riscv/riscv-pk
* Privileged Spec: 1.9.1
* User Spec: 2.0
* ABI:

## OpenSBI
* Maintainer(s): Anup Patel
* Version: 0.3
* Status: 
* Upstreaming status:
* Future work:
* Upstream repository: https://github.com/riscv/opensbi
* Privileged Spec: 1.9.1
* User Spec:
* ABI:

# OS and OS kernels

## Linux built from source

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
Linux Kernel | [github](https://github.com/riscv/riscv-linux), [kernel.org](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git) | GPLv2 | Andrew Waterman (SiFive), Albert Ou (SiFive), Palmer Dabbelt (SiFive)
Yocto Project/OpenEmbedded | [github](https://github.com/riscv/meta-riscv) |  | Khem Raj
Poky | [github](https://github.com/riscv/riscv-poky) |  | Martin Maas (University of California, Berkeley)
Buildroot | [busybox.net](https://git.busybox.net/buildroot/) |  | Mark Corbin (Embecosm)

## Linux distributions

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
Fedora	| [fedoraproject.org](http://fedoraproject.org/wiki/Architectures/RISC-V) | | Richard WM Jones, Stefan O’Rear, David Abdurachmanov
Debian | [debian wiki](https://wiki.debian.org/RISC-V), [mit.edu](http://riscv.mit.edu/), [riscv.org](https://content.riscv.org/wp-content/uploads/2016/07/Wed1115_Working_Towards_a_Debian_RISC-V_Port.pdf), [Annc](https://people.debian.org/~mafm/posts/2017/20170422_debian-gnulinux-port-for-risc-v-64-bit-riscv64/) | | Manuel A. Fernandez Montecelo
OpenMandriva | [openmandriva.org](http://abf-downloads.openmandriva.org/cooker/repository/riscv64/), [openmandriva.org](http://openmandriva.org/) | | Bernhard "Bero" Rosenkränzer
openSUSE | [opensuse.org](https://build.opensuse.org/project/show/openSUSE:Factory:RISCV) |  | Andreas Schwab (SUSE)
Gentoo | [github](https://github.com/palmer-dabbelt/riscv-gentoo) |  | Palmer Dabbelt (University of California, Berkeley)
Parabola GNU/Linux-libre | [github](https://github.com/oaken-source/parabola-riscv64-bootstrap), [parabola.nu](https://git.parabola.nu/abslibre.git) | | Andreas Grapentin (University of Potsdam, HPI)
januslinux | [github](https://github.com/JanusLinux/janus) |  | nee-san

## Real-time Operating Systems

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
embOS | [Website](https://www.segger.com/embOS), [RISC-V port](https://www.segger.com/products/rtos/embos/supported-cores-compiler/sifive/risc-v/embos-riscv-es/) | SEGGER commercial license, free for non-commercial use | [SEGGER](https://www.segger.com/)
RTEMS | [rtems.org](https://git.rtems.org/rtems/), [docs.rtems.org](https://docs.rtems.org/branches/master/user/bsps/bsps-riscv.html#riscv) | | Hesham Almatary
FreeRTOS | [sourceforge](https://www.sourceforge.net/projects/freertos/) [freertos.org](https://www.freertos.org/Using-FreeRTOS-on-RISC-V.html) | | AWS
Zephyr | [github](https://github.com/zephyrproject-rtos/zephyr/), [docs](http://docs.zephyrproject.org/boards/riscv32/index.html) | | Karol Gugala (Antmicro), Peter Gielda (Antmicro), Nathaniel Graff (SiFive)
NuttX | [bitbucket.org](https://bitbucket.org/nuttx/nuttx/src/master/), [nuttx.org](http://nuttx.org/Documentation/NuttX.html#riscv) | | 
Apache Mynewt | [riscv.org](https://riscv.org/wp-content/uploads/2016/07/Wed930_riscv_apachemynewt_v1.2.pdf) | | James Pace, Runtime
OpenWrt | [github](https://git.openwrt.org/?p=openwrt/staging/wigyori.git;a=shortlog;h=refs/heads/kitchensink-201810), [binary repo](http://openwrt.uid0.hu) | | Zoltan Herpai
seL4 | [github](https://github.com/heshamelmatary/sel4riscv-manifest/blob/master/sel4test-06032018.xml), [announcement](http://heshamelmatary.blogspot.com.au/2017/06/update-sel4risc-v-smp-support-sel4.html) | | Hesham Almatary and Data61/CSIRO


## BSD distributions

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
FreeBSD | [github](https://github.com/freebsd/freebsd), [wiki.freebsd.org](https://wiki.freebsd.org/riscv), [presentation](https://riscv.org/wp-content/uploads/2016/01/Tues1445-freebsd-riscv-1.pdf) | | Ruslan Bukin (FreeBSD)
NetBSD | [netbsd.org](http://cvsweb.netbsd.org/bsdweb.cgi/src/?only_with_tag=MAIN), [github](https://github.com/jsonn/src) |  | Matt Thomas (NetBSD), Reinoud Zandijk (NetBSD)

# Compilers and runtimes for other languages

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
Go	| [Upstream](https://github.com/golang/go), [RISC-V repository](https://github.com/riscv/riscv-go), [Stef's fork](https://github.com/sorear/golang-go) | BSD 3-clause	| Benjamin Barenblat (Google), Michael Pratt (Google), Stef O'Rear
Ocaml	| [Upstream](https://github.com/ocaml/ocaml), [RISC-V repository](https://github.com/nojb/riscv-ocaml)	| LGPL	| Nicolás Ojeda Bär
Maxine VM (Java Virtual Machine)	| [Upstream](https://github.com/beehive-lab/Maxine-VM)	| GPLv2	| Maxine team
Jikes RVM (Java Virtual Machine)	| [Upstream](https://github.com/JikesRVM/JikesRVM)	| Eclipse Public License (EPL)	| Martin Maas (University of California, Berkeley)
OpenJDK/HotSpot (Java Virtual Machine)	| ?	| ?	| Alexey Baturo, Michael Knysnek, Martin Maas
Free Pascal	| [Upstream](https://svn.freepascal.org/cgi-bin/viewvc.cgi/trunk/)	| ?	| Jeppe Johansen and others
Nim	| [Upstream](https://nim-lang.org/)	| MIT	| Andreas Rumpf and others
Ada (GNAT)	| [Upstream](https://gcc.gnu.org/viewcvs/gcc/trunk/)	| Proprietary	| [AdaCore](http://adacore.com)
Rust	| [Upstream](https://github.com/rust-lang/rust/)	| Apache and MIT	| [Rust Project](https://www.rust-lang.org/)
muForth	| [Upstream](https://github.com/nimblemachines/muforth)	| ?	| David Frech
ibForth	| [Upstream](https://github.com/larsbrinkhoff/lbForth)	| GPLv3	| Lars Brinkhoff
Mecrisp-Quintis Forth kernel	| [Upstream](http://mecrisp.sourceforge.net/)	| ?	| Matthias Koch

# IDEs

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
GNU MCU Eclipse | [Website](https://gnu-mcu-eclipse.github.io), [Repositories](https://github.com/gnu-mcu-eclipse), [Binary distribution](https://github.com/gnu-mcu-eclipse/org.eclipse.epp.packages/releases/) |	EPL-1.0 / various	| Liviu Ionescu
Embedded Studio | [Website](https://www.segger.com/embeddedstudio), [RISC-V spec](https://www.segger.com/products/development-tools/embedded-studio/editions/risc-v/) | SEGGER commercial license, free for non-commercial use | [SEGGER](https://www.segger.com/)


# Security

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
emCrypt | [Website](https://www.segger.com/emcrypt) | SEGGER commercial license, free for non-commercial use | [SEGGER](https://www.segger.com/)
Hex Five Security | [SDK](https://github.com/hex-five/multizone-sdk) |	Proprietary	| [Hex Five Security Inc.](http://www.hex-five.com/)
Keystone Enclave | [Website](https://keystone-enclave.org), [Repositories](https://github.com/keystone-enclave) | BSD 3-clause | [Keystone Team](https://keystone-enclave.org/contact/)
SecureRF | [Website](https://www.securerf.com/products/), [SDK](https://info.securerf.com/iot-embedded-sdk-development-kit) | Proprietary | [SecureRF Corp.](https://www.securerf.com)
CoreGuard | [Website](https://www.dovermicrosystems.com/solutions/coreguard/) | Proprietary | [Dover Microsystems, Inc.](https://www.dovermicrosystems.com/get-coreguard) 

# Help Wanted

* V8
* Node.js
* Dart
