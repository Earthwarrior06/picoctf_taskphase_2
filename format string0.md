# format string 0

**Flag:** `picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_74f6c0e7}`

How you approached the challenge:

- step 1
Looking at the previous question I just thought i could try the same thing
```bash
earthwarrior@LAPTOP-VLDN28C5:~$ nc mimas.picoctf.net 59065
Welcome to our newly-opened burger place Pico 'n Patty! Can you help the picky customers find their favorite burger? Here comes the first customer Patrick who wants a giant bite. Please choose from the following burgers: Breakf@st_Burger, Gr%114d_Cheese, Bac0n_D3luxe 
Enter your recommendation: &&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
There is no such burger yet!

picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_74f6c0e7}
```

What you learned through solving this challenge:

1. first concept
2. second concept
3. etc.

Other incorrect methods you tried:

I thought I could make the code fail if I put special characters in
```bash
earthwarrior@LAPTOP-VLDN28C5:~$ nc mimas.picoctf.net 59065
Welcome to our newly-opened burger place Pico 'n Patty! Can you help the picky customers find their favorite burger?
Here comes the first customer Patrick who wants a giant bite.
Please choose from the following burgers: Breakf@st_Burger, Gr%114d_Cheese, Bac0n_D3luxe
Enter your recommendation: 1e2qwe21.#\
There is no such burger yet!
```


