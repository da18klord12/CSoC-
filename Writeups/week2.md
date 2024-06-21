# Writeups for CSoC Infosec Week - 2
## Cryptohack Challenges

> # Introduction
    1. Finding Flags : flag is mentioned in the description  of this challenge 

    2. Great Snakes : 
                    open terminal
                    wget "<file link>"
                    chmod +x <greatsnakes file>
                    ./greatsnakes.py

                    after execution you will get the flag

    3. Network Attacks : 
                    wget "<file link>"
                    chmod +x <pwntools file>
                    vim pwntoolsf       

                    in the script make some changes 
                    buy="flag"
                    
                    now execute this file and u will get flag

> # General
## Encoding 
### 1. ASCII

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/asciinew.png)

### 2. Hex

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/hexscript.png)

### 3. Base 64

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/base64.png)

### 4. Bytes and Big Integers

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/bytesandbigintegers.png)

## XOR
### XOR Starters

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/xorstart.png)

### XOR Properties

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/xorprop.png)

> was stuck in writing the scripts for other 2

## MATHEMATICS
### Greatest Common Divisor

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/gcd.png)

### Extended GCD

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/extendedgcd.png)

### Modular Arithmeatic 1

![scipt](https://github.com/da18klord12/CSoC-/blob/main/scripts/modulararth1.png)

> for Modular Artihmatic 2 and Modular inverting will upload it later, still on it and others too

### Challenge 1 : 
it looked like a base64 so decoded it and it gave me a new python script.....as far as i can, it seems that the new script i got on decoding is some used for decoding a flag which is stored in flag.txt
Below is my script for decoding and what i got after decoding 

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/challenge1.png)
![output](https://github.com/da18klord12/CSoC-/blob/main/scripts/output.png)
> Challenge 1 part 2:
in this file which was named as output in the repo first i tried to use it as flag.txt and executed the previous script but got nothing and then using another script i tried to decrypt but it was somewhat distorted and as if it was originally something like CSOC23{...} even on online platforms it was somewhat like this

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/part2chall2.png)
and the output is below
![output](https://github.com/da18klord12/CSoC-/blob/main/scripts/part2out.png)

### Challenge 2 :
After looking at this I made a note that it was a string comprising of several strings with different encodings

![script](https://github.com/da18klord12/CSoC-/blob/main/scripts/challenge2.png)




