# Custom encrytion

**Flag:** `picoCTF{custom_d2cr0pt6d_dc499538}`

How you approached the challenge:

## step 1
First i converted the code to get the key into a code with all the fuctions simplified and printed them to see what values they held 
```bash
a=89
b=27
u= (31**a)%97
v= (31**b)%97
print(u,v)
key= (v**a)%97
b_key= (u**b)%97
print(key,b_key)
if key == b_key:
    shared_key = key

```

## step 2
Since I found the value of the shared_key through the above code and are given the value of cipher_text
I wrote the code(inverse of "encrypt(semi_cipher, shared_key)" function) to get the value of semi_cipher 
```bash
semi_cipher= ""
for i in [33588, 276168, 261240, 302292, 343344, 328416, 242580, 85836, 82104, 156744, 0, 309756, 78372, 18660, 253776, 0, 82104, 320952, 3732, 231384, 89568, 100764, 22392, 22392, 63444, 22392, 97032, 190332, 119424, 182868, 97032, 26124, 44784, 63444]:
    semi_cipher+= chr(int(i/(shared_key*311))) #will be int since i= (ord(semi_cipher))*shared_key*311

print(semi_cipher) #just to see the value 

```

## step 3
Then i found the (inverse of the "dynamic_xor_encrypt(plaintext, text_key)" function) code to get the value of the input (plain_text)
```bash
cipher_text = semi_cipher
print(len(cipher_text))
text_key="trudeau"
key_length = len(text_key)
i=0
flag_bwd=""
for enc_char in cipher_text:
    key_char = text_key[i % key_length]
    char = chr(ord(enc_char)^ord(key_char))
    flag_bwd+=char
    i+=1
print(flag_bwd[::-1])
```
## Code(overall)
```bash
a=89
b=27
u= (31**a)%97
v= (31**b)%97
print(u,v)
key= (v**a)%97
b_key= (u**b)%97
print(key,b_key)
if key == b_key:
    shared_key = key

semi_cipher= ""
for i in [33588, 276168, 261240, 302292, 343344, 328416, 242580, 85836, 82104, 156744, 0, 309756, 78372, 18660, 253776, 0, 82104, 320952, 3732, 231384, 89568, 100764, 22392, 22392, 63444, 22392, 97032, 190332, 119424, 182868, 97032, 26124, 44784, 63444]:
    semi_cipher+= chr(int(i/(shared_key*311)))#will be int since i= (ord(semi_cipher))*shared_key*311

print(semi_cipher)

cipher_text = semi_cipher
print(len(cipher_text))
text_key="trudeau"
key_length = len(text_key)
i=0
flag_bwd=""
for enc_char in cipher_text:
    key_char = text_key[i % key_length]
    char = chr(ord(enc_char)^ord(key_char))
    flag_bwd+=char
    i+=1
print(flag_bwd[::-1])
```
## Output(overall)
```bash
49 85
12 12
	JFQ\XA* SD V>3 1
34
picoCTF{custom_d2cr0pt6d_dc499538}
```

![screenshot](./screenshot.png)

What you learned through solving this challenge:

1. The inverse of " ^ "(XOR operator) is " ^ "
   since it works by checking the binary form of number and comparing "1"s and "0"s
   ```bash
   6^3 ==> 5
   5^3 ==> 6
   6^5 ==> 3
   6 = 0000000000000110
   3 = 0000000000000011
   5 = 0000000000000101
   ```
2. The inverse of ord is chr and vice versa (ord function converts a character to its unicode value and chr does the opposite)

References

- [reference 1](https://www.w3schools.com/python/python_operators.asp)
- [reference 2](https://www.geeksforgeeks.org/enumerate-in-python/)


