# secureSeed
Simple secure BIP39 seed generation for paranoid crypto HODLERS

A variety of wallets are now using BIP39 seeds for hierarchical address generation.  This greatly improves security so long as the random number generator can be trusted.  Because it's difficult to verify the integrity/security of a random number generater, I thought it'd be best to allow users to generate their own random seed, eliminating the need to trust some other generator.

This code allows you to generate your own BIP39 seed by generating the 256 bits that constitute your key via a method you choose (I recommend flipping a coin 256 times).  You can manually enter the bits inside the "seedBits.dat" file.  When you run the code it will output the corresponding BIP39 mnemonic.

WARNING
It is recommended you only execute this code on an isolated machine that will NEVER be connected to the internet.  It's possible your machine could be compromised and if connected to the internet an attacker could conceivably gain access to your secret seed if you've used this code to store it.  To ensure your security it is recommended that this code be executed on an isolated raspberry pie that you destroy or at least wipe after using it to generate your secure seed.


DISCLAIMER
The majority of this code is dedicated to calculating the SHA256 checksum of the seed.  I did not write that code, I copied it from another github user hak8or:
https://gist.github.com/hak8or/8794351

