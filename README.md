# quic-hmvm-hexagonMVM
 https://source.codeaurora.org/quic/hmvm/hexagonMVM
 
 https://wiki.codeaurora.org/xwiki/bin/HexagonMiniVM/
 

Hexagon MiniVM
Last modified by Rob Garth on 2016/05/20 20:41
Hexagon MiniVM

MiniVM is a basic reference implementation of the Hexagon Virtual Machine.  It is intended to provide the bare minimum functionality needed to allow a single paravirtualized guest (like the Linux kernel) to run.

This implementation only runs on Hexagon architectures v2 and v3 and is provided as-is for reference.
Release Tags

INITIAL_RELEASE - First public release of the Hexagon MiniVM
Downloading and Building from Source

Building MiniVM requires a Hexagon toolchain, available from Mentor:

https://sourcery.mentor.com/GNUToolchain/release2422

or

https://sourcery.mentor.com/GNUToolchain/release2331

You may need to edit the compiler prefix in the Makefile depending on which toolchain you choose.

$ git clone git@codeaurora.org/quic/hmvm/hexagonMVM.git

$ make -C hexagonMVM GUEST_ENTRY=[guest entry point]

Exact details of loading/bootup may vary depending on platform, but MiniVM should be loaded at a 64k aligned address, out of the way of the guest OS.  Once it finishes its own initialization, it will jump to the guest OS's entry point.
Licenses

The source code available for download from Code Aurora may be covered by one or more different licenses. The files in Code Aurora may contain changes and additions on top of the code from the original source. These changes and additions are covered under the same license as the original source. In many cases, the license is explicitly listed at the beginning of the file. A list of licenses is included for reference purposes only.

    Clear BSD: http://directory.fsf.org/wiki/License:ClearBSD



