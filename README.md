
# Implementing Standard Blowfish Encryption Algorithm

Using a standard Blowfish implementation as basic encryption, write a code for the
CBC and OFB modes.
## Implementation details


Blowfish is significantly faster than DES and provides a good encryption rate with
no effective cryptanalysis technique found to date.
It is one of the first, secure block cyphers not subject to any patents and hence
freely available for anyone to use.
blockSize:
 64-bits
keySize:
 32-bits to 448-bits variable size
number of subkeys:
 18 [P-array]

number of rounds:
 16
number of subsitution boxes:
 4 [each having 512 entries of 32-bits each]

Blowfish Encryption Algorithm:

The entire encryption process can be elaborated as:

Step1:
 Generation of subkeys:

18 subkeys{P[0]
…P[17]
} are needed in both encryption aswell as decryption process
and the same subkeys are used for both the processes.
These 18 subkeys are stored in a P-array with each array element being a 32-bit
entry.
It is initialised with the digits of pi(?)
.
The hexadecimal representation of each of the subkeys is given by:

P[0]
 = "243f6a88"
..
P[17]
 = "8979fb1b"
Step2:
 initialise Substitution Boxes:

4 Substitution boxes(S-boxes)
 are needed{S[0]
…S[4]
} in both encryption aswell as
decryption process
with each S-box having 256 entries{S[i]
[0]
…S[i]
[255]
, 0&lei&le4} where each entry
is 32-bit.
It is initialised with the digits of pi(?)
 after initialising the P-array.
Step3:
 Encryption:

The encryption function consists of two parts:

Rounds:
 The encryption consists of 16 rounds with each round(Ri)
 taking inputs the 
plainText(P.T.)
 from previous round and corresponding subkey(Pi)
.
Post-processing:
 The output after the 16 rounds is processed further.
Blowfish Decryption Algorithm:

18 subkeys{P[0]
…P[17]
} are needed in both encryption aswell as decryption process
and the same subkeys are used for both the processes.
These 18 subkeys are stored in a P-array with each array element being a 32-bit
entry.
It is initialised with the digits of pi(?)
.
The hexadecimal representation of each of the subkeys is given by:

P[0]
 = "243f6a88"
..
P[17]
 = "8979fb1b"
Step2:
 initialise Substitution Boxes:

4 Substitution boxes(S-boxes)
 are needed{S[0]
…S[4]
} in both encryption aswell as
decryption process
with each S-box having 256 entries{S[i]
[0]
…S[i]
[255]
, 0&lei&le4} where each entry
is 32-bit.
It is initialised with the digits of pi(?)
 after initialising the P-array. 
## Screenshots

![](https://user-images.githubusercontent.com/44118554/140687841-094b34a1-4f97-422a-ba72-40f9b4eb23a7.PNG)

![](https://user-images.githubusercontent.com/44118554/140687913-4531ea6b-87c7-4159-8fee-c65e5cd5d151.PNG)

![](https://user-images.githubusercontent.com/44118554/93970149-1e5e4f00-fd8b-11ea-9a4f-a498bd7d23df.png)

![](https://user-images.githubusercontent.com/44118554/140687453-8c34a48c-e6d5-45ab-aa6b-258a9a163163.PNG)




## Run Locally

Clone the project

```bash
  git clone https://github.com/RohitHansdah/blowfish
```

Go to the project directory

```bash
  cd code.py
```

Install dependencies

```bash
  pip install tk
```




## Demo

![GIF](https://i.makeagif.com/media/11-08-2021/5PBtSK.gif)


## Documentation

[Report](https://drive.google.com/file/d/1MovE4F-sgK2WGRk9Ujr32b-zMa2C1lfc/view?usp=sharing)


## Conclusion

Advantages and Disadvantages of Blowfish Algorithm:

1.)
Blowfish is a fast block cipher except when changing keys. Each new key requires
a pre-processing equivalent to 4KB of text.

2.)It is faster and much better than DES Encryption.

3.)Blowfish uses a 64-bit block size which makes it vulnerable to birthday attacks.

4.)A reduced round variant of blowfish is known to be suceptible to known plain
text attacks(2nd order differential attacks – 4 rounds).