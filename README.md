# NXcrypt

NXcrypt is a polymorphic 'python backdoors' crypter written in python by Hadi Mene (h4d3s) .
The output  is fully undetectable .
NXcrypt can inject malicious python file in a output executed in the same time with a normal file

- In Linux , run it as root
- NXcrypt encrypted output is 99% FUD 

# Usage :

- sudo  ./NXcrypt.py --file=backdoor.py --output=output_backdoor.py # encrypt backdoor.py and output file is output_backdoor.py
- sudo ./NXcrypt.py --file=shell.py # encrypt shell.py and default output file  is backdoor.py but you can edit it in source code
 - sudo ./NXcrypt.py --help # NXcrypt help
 - sudo ./NXcrypt.py --backdoor-file=payload.py --file=test.py --output=hacked.py # inject payload.py with  test.py into hacked.py with multi-threading system
 # How it work ? 
 
 Encryption module :
 
 - NXcrypt add some junkcode .
 - NXcrypt use a python internal module 'py_compile' who compile the code into bytecode to a .pyc file .
 - NXcrypt convert .pyc file into normal .py file .
 - And in this way we can obfuscate the code
 - The md5sum will change too
 
Injection  module
- it inject a malicious python file  into a normal file injected in the same time and  save into an output with multi-threading system

 # Test with Virustotal
 
 Before :
 
SHA256:	e2acceb6158cf406669ab828d338982411a0e5c5876c2f2783e247b3e01c2163
File name:	facebook.py
Detection ratio:	2 / 54

After :

SHA256:	362a4b19d53d1a8f2b91491b47dba28923dfec2d90784961c46213bdadc80add
File name:	facebook_encrypted.py
Detection ratio:	0 / 55


# Credits

All Credits go to Suspicious Shell Activity team

# Video Tutorial

https://www.youtube.com/watch?v=s8Krngv2z9Q


 
 


 
