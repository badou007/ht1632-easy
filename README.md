ht1632-easy
===========
see the result at http://youtu.be/fplK7FjgmwI

to use the code beware the #defines at the beginning to correctly connect the master to the atmega16 .
on sure electronic cable cs2,cs1,wr and data are in this order on the side of the the "détrompeur" ,cs2 at the top near the red line and cs2 first .after cs2 on the other side are cs3 and cs4 with cs3 at the top .
there lot of explanations to help beginner to understand what is going .
it's strongly recommanded to read carefully the datasheet from Holtek , this helps you tounderstand what is going .

writing to each panel uses the continuous writing mode . I use a matrix J1[96] that I share in 3 parties: from 0 to 31 , from 31 to 63 and from 64 to 95 .

you can modify the code to connect 4 pannels : simply modify the J1[96] TO J1[128],add annother function affiche3 for the forth pannel , modify the functions affiche : the first from 0 to 31 , second from 32 to 63, 3eme from 64 to 95 and the master from 96 to 127 ; add functions c3_hight() and cs3_low() following the cs3 PIN , modify the ht1632_command1 to take acount of the forth panel and add |(1<<cs3) to ht1632_data_dir|=(1<<cs)|(1<<data)|(1<<wr)|(1<<cs1)|(1<<cs2) in the int() function ; I believe it's all ; 
now remark that achieving to drive 3 pannels the same program can drive 1 or 2 pannels ; the same for dring 4 panels allows to drive 1 or 2 or 3 panels .

OK!!

