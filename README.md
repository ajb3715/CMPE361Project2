The purpose of this program is to securely encrypt/decrypt user provided plaintext.
The implemented feature of this method was Masking, which functions similar to an
additional Key and mixes itself into the data. The Key is provided by the user, 
while the mask is generated randomly by polling the system time at the start of an
encryption request.


4 Commands can be provided to the system

target.simpleserial_write('l',16,key) - Provides the Key utilized for encryption
target.simpleserial_write('r',16,timeout = 500) - reads data from the system with a timout before continuing to next operation
target.simpleserial_write('e',16,plain) - provides the plaintext for encryption
target.simpleserial_write('d',16,encrypted) - provides the ciphertext for decryption

Jupyter notebook can be utilized to communicate with the system to provide the commands listed above.

The entire functionality of the code can be found within:
CMPE361_Project2\Project2\hardware\victims\firmware\simpleserial-aes\simpleserial-aes.c



