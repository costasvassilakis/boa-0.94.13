# Boa 0.94.13
[![Total alerts](https://img.shields.io/lgtm/alerts/g/shrugly/boa-0.94.13.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/shrugly/boa-0.94.13/alerts/)
[![Language grade: C/C++](https://img.shields.io/lgtm/grade/cpp/g/shrugly/boa-0.94.13.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/shrugly/boa-0.94.13/context:cpp)
[![Build Status](https://travis-ci.org/shrugly/boa-0.94.13.svg?branch=master)](https://travis-ci.org/shrugly/boa-0.94.13)

[Boa](http://www.boa.org/) is a simple and lightweight HTTP server which is occasionally still found in embedded firmware images for serving CGI scripts, files, and more. 0.94.13 is the last stable version, and was released [in 2002](https://en.wikipedia.org/wiki/Boa_(web_server)).

## Changes

This repository contains Boa 0.94.13 with minimal changes. It should not be considered meaningfully enhanced from the original source. However, it does contain some integrations and output from tools to help identify security hotspots and bad practices.

### Code

2020-05-09 - Mirrored tarball of idlookup-1.2 from Peter Eriksson to `extras/`, required by `examples/cgi-test.cgi` and `examples/nph-test.cgi`
2020-05-08 - Fixed preprocessing token error in `src/compat.h`, which was preventing compilation.

### Integrations

- [LGTM](https://lgtm.com/) - performs QL-based quality and security checks on the main repository as well as any PRs to help identify & track security hotspots.
- [Travis CI](https://travis-ci.org/) - builds Boa on Linux and macOS with GCC & Clang to ensure that changes don't immediately introduce quality issues.

### security/*.txt

Some SAST tools are run manually on the latest version of this software to identify potential hotspots. Listed in increasing order of complexity, they are:
* [flawfinder](https://dwheeler.com/flawfinder/) - scans for potentially insecure functions being used in C programs.
* [cppcheck](http://cppcheck.sourceforge.net/) - performs flow sensitive analysis to check C/C++ code for undefined behavior.
* [infer](https://fbinfer.com/) - a modular verification and analysis engine that checks Java/C/Obj-C code for null pointer dereferences and resource or memory leaks.

Summary 2020-05-08: Boa does not conform to modern, secure coding practices - which is expected - and has a number of potentially severe issues to investigate.

## SHRuG Creed

We apply security tools & processes to assist developers in determining if legacy software is the right choice for their application. Where reasonable we will attempt to upgrade the security, reliability, and quality of legacy software.

However, we are not volunteering to be new maintainers for this software. We will not develop new features or substantially change its functionality. Please report bugs that result in security problems to us using the [Issues](https://github.com/shrugly/boa-0.94.13/issues) tab and we will look into fixing them. Other bugs, feature requests, usability issues, etc. will be largely ignored or closed without warning.

### Warranty & Liability

This work is licensed under the GNU GPLv2. This includes modifications by the SHRuG working group. In particular, we'd like to remind you of the "NO WARRANTY" section, as follows:

11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.

12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.
