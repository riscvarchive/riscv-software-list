# RISC-V Software Ecosystem Overview

This document captures the status of the RISC-V Software Ecosystem. Please add
to the list and fix inaccuracies by making a Pull Request against the [software list repository on GitHub](https://github.com/riscv/riscv-software-list).

* [Simulators](#simulators)
* [Object toolchain](#object-toolchain)
* [Debugging](#debugging)
* [C compilers and libraries](#c-compilers-and-libraries)
* [Boot loaders and monitors](#boot-loaders-and-monitors)
* [Hypervisor and related tools](#hypervisors-and-related-tools)
* [OS and OS kernels](#os-and-os-kernels)
* [Compilers and runtimes for other languages](#compilers-and-runtimes-for-other-languages)
* [IDEs, SDKs and binary toolchain distributions](#ides-sdks-and-binary-toolchain-distributions)
* [Security](#security)
* [Machine Learning / AI](#machine-learning--ai)

**We would like to enlist community help for the software ports in the [Help Wanted](#help-wanted) section.**

# Simulators

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
DBT-RISE-RISCV | [github](https://github.com/Minres/DBT-RISE-RISCV) | BSD 3-Clause | [MINRES Technologies](https://www.minres.com/)
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
WebRISC-V | [github](https://github.com/Mariotti94/WebRISC-V)| BSD 3-clause | Gianfranco Mariotti, Roberto Giorgi  (University of Siena)
PQSE | [website](https://pqsoc.com/software/) | Proprietary | [PQShield](https://pqshield.com)
riscv-rust | [website](https://takahirox.github.io/riscv-rust/index.html) [github](https://github.com/takahirox/riscv-rust) | MIT | Takahiro Aoyagi
terminus | [github](https://github.com/shady831213/terminus) | MIT | [Yang Li](https://github.com/shady831213)
Vulcan   | [github](https://github.com/vmmc2/Vulcan) | MIT | [Victor Miguel de Morais Costa](https://github.com/vmmc2)

# Object toolchain

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
Binutils | [RISC-V repo](https://github.com/riscv/riscv-binutils-gdb), [Upstream repos](https://sourceware.org/git/gitweb.cgi?p=binutils-gdb.git) | GPLv2 | Andrew Waterman (SiFive), Palmer Dabbelt (Google) & Jim Wilson (SiFive)
LLVM | [GitHub mirror](https://github.com/llvm/llvm-project/tree/master/llvm/lib/Target/RISCV) | Apache 2.0 with LLVM exception | Alex Bradbury (lowRISC)
Cranelift | [GitHub](https://github.com/CraneStation/cranelift) | Apache 2.0 | [Cranelift core team](https://github.com/orgs/CraneStation/people/)

# Debugging


Name | Links | License | Maintainers
---- | ----- | ------- | -----------
GDB | [Upstream](https://sourceware.org/git/gitweb.cgi?p=binutils-gdb.git) | GPLv2 | Andrew Burgess (Embecosm), Palmer Dabbelt (Google)
OpenOCD | [Upstream repo](https://sourceforge.net/p/openocd/code/ci/master/tree/), [RISC-V repo](https://github.com/riscv/riscv-openocd) | GPLv2 | Tim Newsome (SiFive), Megan Wachs (SiFive), Palmer Dabbelt (Google)
GNU MCU Eclipse OpenOCD | [Website](https://gnu-mcu-eclipse.github.io/openocd/), [GitHub](https://github.com/gnu-mcu-eclipse/openocd) | GPLv2 | Liviu Ionescu
TRACE32 JTAG Debugger | [Website](https://www.lauterbach.com/bdmriscv.html) | TRACE32 license | [Lauterbach](https://www.lauterbach.com)
Ozone - the J-Link Debugger | [Website](https://www.segger.com/ozone) | SEGGER commercial license (J-Link PLUS) | [SEGGER](https://www.segger.com/)
Ashling RiscFree Debugger | [Website](https://www.ashling.com/ashling-riscv/) | Ashling commercial license| [Ashling](http://www.ashling.com/)
Imperas Multi Processor Debugger | [Website](http://www.imperas.com/riscv#debug) | Imperas Commercial License | [Imperas](http://www.imperas.com/)
TCF Debugger | [Website](https://projects.eclipse.org/projects/tools.cdt.tcf), [GitHub](https://github.com/eclipse/tcf.agent) | Eclipse Distribution License 1.0 (BSD) / Eclipse Public License 1.0 | Sanimir Agovic
PlatformIO Unified Debugger | [Docs](https://docs.platformio.org/en/latest/plus/debugging.html) | Apache 2.0 | [PlatformIO](https://platformio.org/)

# C compilers and libraries

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
GCC	| [Upstream](https://gcc.gnu.org/git/gitweb.cgi?p=gcc.git), [RISC-V repository](https://github.com/riscv/riscv-gcc) | GPLv3	| Andrew Waterman (SiFive), Palmer Dabbelt (Google), Jim Wilson (SiFive), Kito Cheng (SiFive)
GNU MCU Eclipse RISC-V Embedded GCC (riscv-non-embed-gcc)	| [Web](https://gnu-mcu-eclipse.github.io/toolchain/riscv/), [Repository](https://github.com/gnu-mcu-eclipse/riscv-none-gcc), [Build](https://github.com/gnu-mcu-eclipse/riscv-none-gcc-build), [Binary package installer](https://www.npmjs.com/package/@gnu-mcu-eclipse/riscv-none-gcc)	| Eclipse Public License |	Liviu lonescu
Clang/LLVM	| [Upstream](https://github.com/llvm/llvm-project)	| Apache 2.0	| Alex Bradbury (lowRISC)
CompCert	| [Upstream](https://github.com/AbsInt/CompCert.git)	| INRIA Non-Commercial License Agreement	| Xavier Leroy
Glibc	| [Upstream](https://sourceware.org/git/?p=glibc.git), [RISC-V repository](https://github.com/riscv/riscv-glibc) |	GPLv2 |	Palmer Dabbelt (Google), Andrew Waterman (SiFive), DJ Delorie (Red Hat), Darius Rad(Bluespec)
Newlib	| [Upstream](http://cygwin.com/git/gitweb.cgi?p=newlib-cygwin.git), [RISC-V repository](https://github.com/riscv/riscv-newlib)	| GPLv2	| Kito Cheng (SiFive)
SEGGER Runtime Library | [Website](https://www.segger.com/products/development-tools/runtime-library/) | SEGGER commercial license | [SEGGER](https://www.segger.com/)
SEGGER Floating Point Library | [Website](https://www.segger.com/products/development-tools/runtime-library/technology/floating-point-library/) | SEGGER commercial license | [SEGGER](https://www.segger.com/)
Musl | [GitHub](https://github.com/riscv/riscv-musl)	| MIT | -

# Boot loaders and monitors

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
coreboot | [Upstream](https://review.coreboot.org/cgit/coreboot.git/) | GPLv2 | Ron Minnich (Google), Jonathan Neuschäfer
U-Boot | [Upstream](https://gitlab.denx.de/u-boot/u-boot) | GPLv2 | Rick Chen (Andes)
Proxy Kernel/BBL | [GitHub](https://github.com/riscv/riscv-pk) | BSD 3-clause | SiFive
OpenSBI | [GitHub](https://github.com/riscv/opensbi) | BSD 2-clause | Anup Patel (Western Digital), Atish Patra (Western Digital)

# Hypervisors and related tools

Name | Links | License | Brief | Maintainers
---- | ----- | ------- | ----- | -----------
Xvisor | [Website](http://xhypervisor.org), [Upstream](https://github.com/xvisor/xvisor.git), [RISC-V Repo](https://github.com/avpatel/xvisor-next.git) | GPLv2 | Type-1 baremetal monolithic hypervisor | Anup Patel (Western Digital)
KVM | [Website](https://www.linux-kvm.org), [RISC-V Repo](https://github.com/kvm-riscv/linux.git), [RISC-V Wiki](https://github.com/kvm-riscv/howto/wiki) | GPLv2 | Type-2 hypervisor | Anup Patel (Western Digital), Atish Patra (Western Digital)
KVMTOOL | [Upstream](https://git.kernel.org/pub/scm/linux/kernel/git/will/kvmtool.git), [RISC-V Repo](https://github.com/kvm-riscv/kvmtool.git)  | GPLv2 | Userspace tool for the KVM hypervisor | Anup Patel (Western Digital), Atish Patra (Western Digital)

# OS and OS kernels

## Linux built from source

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
Linux Kernel | [github](https://github.com/riscv/riscv-linux), [kernel.org](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git) | GPLv2 | Andrew Waterman (SiFive), Albert Ou (SiFive), Palmer Dabbelt (Google)
Yocto Project/OpenEmbedded | [github](https://github.com/riscv/meta-riscv) | MIT | Khem Raj
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
Ataraxia Linux | [github](https://github.com/ataraxialinux/ataraxia) |  | protonesso

## Real-time Operating Systems

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
embOS | [Website](https://www.segger.com/embOS), [RISC-V port](https://www.segger.com/products/rtos/embos/supported-cores-compiler/sifive/risc-v/embos-riscv-es/) | SEGGER commercial license, free for non-commercial use | [SEGGER](https://www.segger.com/)
RTEMS | [rtems.org](https://git.rtems.org/rtems/), [docs.rtems.org](https://docs.rtems.org/branches/master/user/bsps/bsps-riscv.html#riscv) | | Hesham Almatary
FreeRTOS | [sourceforge](https://www.sourceforge.net/projects/freertos/), [freertos.org](https://www.freertos.org/Using-FreeRTOS-on-RISC-V.html) | MIT | AWS
Zephyr | [github](https://github.com/zephyrproject-rtos/zephyr/), [docs](http://docs.zephyrproject.org/boards/riscv32/index.html) | Apache 2.0 | Karol Gugala (Antmicro), Peter Gielda (Antmicro), Nathaniel Graff (SiFive)
LiteOS | [github](https://github.com/LiteOS/LiteOS_Lab/), [docs](https://www.huaweicloud.com/product/liteos.html) | | Chaifangming (Huawei), Pengzhouhu (Huawei), Huerjia (Huawei)
NuttX | [bitbucket.org](https://bitbucket.org/nuttx/nuttx/src/master/), [nuttx.org](http://nuttx.org/Documentation/NuttX.html#riscv) | | 
Apache Mynewt | [riscv.org](https://riscv.org/wp-content/uploads/2016/07/Wed930_riscv_apachemynewt_v1.2.pdf) | Apache 2.0 | James Pace, Runtime
OpenWrt | [github](https://git.openwrt.org/?p=openwrt/staging/wigyori.git;a=shortlog;h=refs/heads/kitchensink-201810), [binary repo](http://openwrt.uid0.hu) | | Zoltan Herpai
seL4 | [github](https://github.com/seL4/seL4), [seL4.systems](https://sel4.systems/) | GPLv2 (kernel and proofs), various open-source licenses (userland)| [Trustworthy Systems group, Data61 CSIRO](https://ts.data61.csiro.au/)
RT-Thread | [github](https://github.com/RT-Thread), [rt-thread.org](https://www.rt-thread.org/) | Apache 2.0  | RT-Thread
PikeOS | [Press release](https://www.sysgo.com/news-events/news-articles/article/sysgo-adds-risc-v-support-to-its-pikeos-real-time-operating-system) | Proprietary | SYSGO
VxWorks | [Press release](https://www.windriver.com/news/press/pr.html?ID=22570) | Proprietary | [Wind River](https://www.windriver.com)
Embox | [github](https://github.com/embox/embox), [embox.rocks](http://www.embox.rocks/) |  | Embox

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
OpenJDK/OpenJ9 (Java Virtual Machine)	| [Upstream](https://github.com/eclipse/openj9)	| Eclipse Public License 2.0 (EPLv2) with ClassPath Exception & Apache 2.0	| [Cheng Jin](https://github.com/ChengJin01)
Free Pascal	| [Upstream](https://svn.freepascal.org/cgi-bin/viewvc.cgi/trunk/)	| ?	| Jeppe Johansen and others
Nim	| [Upstream](https://nim-lang.org/)	| MIT	| Andreas Rumpf and others
Ada (GNAT)	| [Upstream](https://gcc.gnu.org/viewcvs/gcc/trunk/)	| GPLv3 with linking exception	| [AdaCore](http://adacore.com)
Rust	| [Upstream](https://github.com/rust-lang/rust/)	| Apache and MIT	| [Rust Project](https://www.rust-lang.org/)
muForth	| [Upstream](https://github.com/nimblemachines/muforth)	| ?	| David Frech
ibForth	| [Upstream](https://github.com/larsbrinkhoff/lbForth)	| GPLv3	| Lars Brinkhoff
Mecrisp-Quintis Forth kernel	| [Upstream](http://mecrisp.sourceforge.net/)	| ?	| Matthias Koch
Mono | [Initial support in upstream](https://github.com/mono/mono/pull/11593) | MIT | [Alex Rønne Petersen](https://github.com/alexrp)
Zen	| [Zen-Lang.org](https://www.zen-lang.org/)	| Commercial, AGPLv3 | [connectFree Corporation](http://connectfree.co.jp/)
V8 (JS)	| [github(by RIOS/Futurewei)](https://github.com/v8-riscv/v8), [github(by PLCT)](https://github.com/isrc-cas/v8-riscv)	| BSD | [RIOS](http://rioslab.org/)/[Futurewei](https://www.futurewei.com/), [PLCT Lab](https://isrc.iscas.ac.cn)

# IDEs, SDKs and binary toolchain distributions

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
GNU MCU Eclipse | [Website](https://gnu-mcu-eclipse.github.io), [Repositories](https://github.com/gnu-mcu-eclipse), [Binary distribution](https://github.com/gnu-mcu-eclipse/org.eclipse.epp.packages/releases/) |	EPL-1.0 / various	| Liviu Ionescu
Embedded Studio | [Website](https://www.segger.com/embeddedstudio), [RISC-V spec](https://www.segger.com/products/development-tools/embedded-studio/editions/risc-v/) | SEGGER commercial license, free for non-commercial use | [SEGGER](https://www.segger.com/)
IAR Embedded Workbench | [Website](https://www.iar.com/iar-embedded-workbench/#!?architecture=RISC-V) | commercial | [IAR Systems](https://www.iar.com/)
PlatformIO | [Website](https://platformio.org/), [IDE](https://platformio.org/platformio-ide), [Docs](https://docs.platformio.org/en/latest/) | Apache 2.0 | [PlatformIO](https://platformio.org/)
Freedom Studio | [Website](https://www.sifive.com/boards) | EPL 1.0/various | [SiFive](https://www.sifive.com/)
Ashling RiscFree<sup>TM</sup> IDE | [Website](https://www.ashling.com/ashling-riscv/)|Ashling commercial license|[Ashling](http://www.ashling.com/)
SoftConsole | [Website](https://www.microsemi.com/product-directory/design-tools/4879-softconsole) | Various, see RN | [Microchip](https://www.microchip.com/)
GCC Sourcery CodeBench Lite | [Website](https://www.mentor.com/embedded-software/toolchain-services/codebench-lite-downloads) | GPLv3 | [Mentor, a Siemens Business](www.mentor.com)
LLVM Sourcery CodeBench Lite | [Website](https://www.mentor.com/embedded-software/toolchain-services/codebench-lite-downloads) | Apache 2.0 | [Mentor, a Siemens Business](www.mentor.com)

# Security

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
emCrypt | [Website](https://www.segger.com/emcrypt) | Commercial, free for non-commercial use | [SEGGER](https://www.segger.com/)
CoreGuard | [Website](https://www.dovermicrosystems.com/solutions/coreguard/) | Proprietary | [Dover Microsystems, Inc.](https://www.dovermicrosystems.com/get-coreguard) 
MultiZone API | [GitHub](https://github.com/hex-five/multizone-api) | ISC | [Hex Five Security Inc.](http://www.hex-five.com/)
Secure IoT Stack | [GitHub](https://github.com/hex-five/multizone-secure-iot-stack) | MIT, GPLv2, GPLv3, Evaluation license | [Hex Five Security Inc.](http://www.hex-five.com/)
MultiZone Security TEE & Enclave | [SDK](https://github.com/hex-five/multizone-sdk), [Enclave](https://github.com/hex-five/multizone-linux) |	Evaluation license | [Hex Five Security Inc.](http://www.hex-five.com/)
Keystone Enclave | [Website](https://keystone-enclave.org), [Repositories](https://github.com/keystone-enclave) | BSD 3-clause | [Keystone Team](https://keystone-enclave.org/contact/)
SecureRF | [Website](https://www.securerf.com/products/), [SDK](https://info.securerf.com/iot-embedded-sdk-development-kit) | Proprietary | [SecureRF Corp.](https://www.securerf.com)
IntrinsicID | [Quiddikey](https://www.intrinsic-id.com/products/quiddikey/) | Proprietary | [Intrinsic ID](https://www.intrinsic-id.com/)
Penglai Enclave | [Website](http://penglai-enclave.systems), [GitHub](https://github.com/Penglai-Enclave) | Mulan PSL v1 | [IPADS](https://ipads.se.sjtu.edu.cn/)
PQSLIB / PQSoC | [Website](https://pqsoc.com) | Proprietary | [PQShield](https://pqshield.com)

# Machine Learning / AI

Name | Links | License | Maintainers
---- | ----- | ------- | -----------
TF Lite | [demo](https://github.com/antmicro/litex-vexriscv-tensorflow-lite-demo), [blog note](https://antmicro.com/blog/2019/12/tflite-in-zephyr-on-litex-vexriscv/) | Apache 2.0 |  [Antmicro](https://antmicro.com) / [Google TF Lite team](https://www.tensorflow.org/lite)
ncnn | [GitHub](https://github.com/Tencent/ncnn) | BSD 3-clause |  [Tencent Open Source](https://opensource.tencent.com/en)

# Help Wanted

* Node.js
* Dart
