# lwc-aead-rtl

This page/repository is created in order to collect and benchmark ASIC implementations of lightweight cryptographic schemes. Our initial focus on on Autheticated Encryption with Associated Data (AEAD), especially, but not limited to, the second round candidates to the NIST Lightweight Cryptography Standardization Process. In the future, we may extend our analysis to other primitives, as well.

Our goal is to have a fair and comprehensive study of different cost/performance trade-offs offered by different schemes, so we appreciate contribution in terms of RTL code of different schemes or collaboration on benchmarking on different ASIC technologies. The benchmarking will be done on the Synopsys tool flow using TSMC 65nm technlogy.

There is a different parallel hardware benchmarking project going on targeting FPGA implementations by Jens-Peter Kaps, William Diehl, Michael Tempelmeier, Farnoud Farahmand, Ekawat Homsirikamol, and Kris Gaj on the ATHENa benchmarking platform: https://cryptography.gmu.edu/athena/index.php?id=LWC. In the spirit of having a uniform benchmarking process, we would like designers to use the same minimum compliance criteria and bus interface proposed by the ATHENa team in https://cryptography.gmu.edu/athena/LWC/LWC_HW_API.pdf, which have passed through several rounds of discussion on the NIST LWC forum.

We also accept implementations acheiving minimum compliance criteria but not the bus interface, but such implementations will be reported separately and not as part of the comparison with fully compliant implementations.

For fairness, the implementations should also have no restrictions that are not mandated by the official specification of the scheme.

We welcome further comments and suggestions either through this thread or privately. We also welcome private comments regarding individual schemes. Please address private comments and implementation packages to lwc-asic-benchmark@googlegroups.com

Please include in the zip file:

1) a text file with the filelist of the rtl sources, ordered in a bottom-up approach, e.g. if a module called rnd_function includes a module called sbox, then the file including sbox should come before the file including rnd_function.

2) a text file with the designer(s) name(s), the scheme and variant title, whether the implementation is targetted towards energy, throughput, area, of side-channel, the formula to calculate throughput from the clock frequency and (if available) expected area in gate equivalents. The design can have multiple goals concurrently. Please also indicate whether you would like the code to be publicly available on the repository or not.

Moderator:
Mustafa Khairallah
School of Physical and Mathematical Sciences
NTU, Singapore
