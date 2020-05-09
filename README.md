# Boa 0.94.13
[![Total alerts](https://img.shields.io/lgtm/alerts/g/harm-reduction/boa-0.94.13.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/harm-reduction/boa-0.94.13/alerts/)
[![Language grade: C/C++](https://img.shields.io/lgtm/grade/cpp/g/harm-reduction/boa-0.94.13.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/harm-reduction/boa-0.94.13/context:cpp)

The last stable version of the Boa webserver, with some security checks &amp; integrations. The badges you see are from LGTM's QL-based quality and security checks.

## security/*.txt

Some SAST tools are run manually on the latest version of this software to identify potential hotspots. Listed in increasing order of complexity, they are:
* [flawfinder](https://dwheeler.com/flawfinder/) - scans for potentially insecure functions being used in C programs.
* [cppcheck](http://cppcheck.sourceforge.net/) - performs flow sensitive analysis to check C/C++ code for undefined behavior.
* [infer](https://fbinfer.com/) - a modular verification and analysis engine that checks Java/C/Obj-C code for null pointer dereferences and resource or memory leaks.