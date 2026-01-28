1.  [Soluciones Bandit](#org080bb02)
    1.  [Level 0](#org3c5c99a)
    2.  [Level 0 -> 1](#orgfabaa53)
    3.  [Level 1 -> 2](#org4ff0852)
    4.  [Level 2 -> 3](#org1634d9c)
        1.  [Contraseña](#orgd1a117e)
    5.  [Level 3 -> 4](#org7271fc8)
        1.  [Contraseña](#org1d201a1)
    6.  [Level 4 -> 5](#org1745a0a)
        1.  [Contraseña](#org2850185)
    7.  [Level 5 -> 6](#org7f20d44)
        1.  [Contraseña](#org223d405)
    8.  [Level 6 -> 7](#org35606aa)
        1.  [Contraseña](#org01732a9)
    9.  [Level 7 -> 8](#orgf36d021)
        1.  [Contraseña](#orga5d8292)
    10. [Level 8 -> 9](#orgb725b90)
        1.  [Contraseña](#org1537ffa)
    11. [Level 9 -> 10](#orge9b1466)
        1.  [Contraseña](#org9d2904a)
    12. [Level 10 -> 11](#org6739c1d)
        1.  [Contraseña](#org63ab518)
    13. [Level 11 -> 12](#orge5acee4)
        1.  [Contraseña](#org723c6ce)
    14. [Level 12 -> 13](#org088dcc2)
        1.  [Contraseña](#org68185ab)
    15. [Level 13 -> 14](#orgb8cd260)
    16. [Level 14 -> 15](#org6434c2e)
        1.  [Contraseña](#org5bf166d)
    17. [Level 15 -> 16](#org953dabc)
        1.  [Contraseña](#orgd75c1b1)
    18. [Level 16 -> 17](#org4dc7d08)
        1.  [Contraseña](#org14a7133)
    19. [Level 17 -> 18](#orga4b6243)
        1.  [Contraseña](#org6c9658f)
    20. [Level 18 -> 19](#org20bcf45)
        1.  [Contraseña](#orgde73b89)
    21. [Level 19 -> 20](#orgba5def9)
        1.  [Contraseña](#org4800fb5)
    22. [Level 20 -> 21](#org0c753e2)
        1.  [Contraseña](#org1c944dc)


<a id="org080bb02"></a>

# Soluciones Bandit

-   Las contraseñas de cada nivel son para el siguiente (lado derecho de la flecha)


<a id="org3c5c99a"></a>

## Level 0

1.  Loggearte con SSH

    ssh -p 2220  bandit0@bandit.labs.overthewire.org


<a id="orgfabaa53"></a>

## Level 0 -> 1

1.  En home de Level 0, hay un readme

> Congratulations on your first steps into the bandit game!!
> Please make sure you have read the rules at <https://overthewire.org/rules/>
> If you are following a course, workshop, walkthrough or other educational activity,
> please inform the instructor about the rules as well and encourage them to
> contribute to the OverTheWire community so we can keep these games free!
> 
> The password you are looking for is: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

1.  Contraseña para el nivel 1: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If


<a id="org4ff0852"></a>

## Level 1 -> 2

1.  Debes leer el archivo `-`
2.  Para que se tome como nombre literal, se usa

    cat ./-

1.  Contraseña para el nivel 2: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx


<a id="org1634d9c"></a>

## Level 2 -> 3

1.  Debes leer el archivo `-- spaces in this filename--`

    cat ./"--spaces in this filename--"


<a id="orgd1a117e"></a>

### Contraseña

MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx


<a id="org7271fc8"></a>

## Level 3 -> 4

1.  Contraseña guardada en archivo oculto

    cd inhere
    cat ...Hiding-From-You


<a id="org1d201a1"></a>

### Contraseña

2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ


<a id="org1745a0a"></a>

## Level 4 -> 5

1.  Contraseña guardada en archivo legible

    cd inhere
    cat ./-file07


<a id="org2850185"></a>

### Contraseña

4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw


<a id="org7f20d44"></a>

## Level 5 -> 6

1.  Contraseña guardada en archivo de 1033 bytes de tamaño

    du -a -b | grep 1033


<a id="org223d405"></a>

### Contraseña

HWasnPhtq9AVKe0dmk45nxy20cvUa6EG


<a id="org35606aa"></a>

## Level 6 -> 7

1.  Encontrar un archivo que pertenezca a bandit7, en el grupo bandit6 de 33 bytes de tamaño

    find / -user bandit7 -group bandit6 -size 33c -exec cat {} +


<a id="org01732a9"></a>

### Contraseña

morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj


<a id="orgf36d021"></a>

## Level 7 -> 8

1.  Encontrar contraseña al costado de la palabra &ldquo;millionth&rdquo; en el archivo data.txt

    grep millionth data.txt


<a id="orga5d8292"></a>

### Contraseña

dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc


<a id="orgb725b90"></a>

## Level 8 -> 9

1.  La contraseña es la única lína que ocurre una sola vez en data.txt

    sort data.txt | uniq -c | grep -w "1"


<a id="org1537ffa"></a>

### Contraseña

4CKMh1JI91bUIZZPXDqGanal4xvAg0JM


<a id="orge9b1466"></a>

## Level 9 -> 10

1.  La contraseña es una de las cadenas que está precedida por varios &ldquo;=&rdquo;

    strings data.txt | grep -E "=+" | less


<a id="org9d2904a"></a>

### Contraseña

FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey


<a id="org6739c1d"></a>

## Level 10 -> 11

1.  La contraseña se encuentra encodificada en base64 en data.txt

    base64 -d data.txt 


<a id="org63ab518"></a>

### Contraseña

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr


<a id="orge5acee4"></a>

## Level 11 -> 12

1.  La contraseña se encuentra encodificada en rot13 en data.txt

    cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'


<a id="org723c6ce"></a>

### Contraseña

7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4


<a id="org088dcc2"></a>

## Level 12 -> 13

1.  La contraseña se encuentra comprimida varias veces en data.txt
2.  Solo usa una combinación entre gzip2, bzip2 y tar.


<a id="org68185ab"></a>

### Contraseña

FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn


<a id="orgb8cd260"></a>

## Level 13 -> 14

1.  No hay contraseña. El archivo ssh.private se usa como contraseña para el siguiente nivel y la contraseña del siguiente se encuentra en /etc/bandit<sub>pass</sub>/bandit14
    
        scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private ~/Descargas
        chmod 700 sshkey.private
        ssh -i sshkey.private bandit14@localhost -p 2220


<a id="org6434c2e"></a>

## Level 14 -> 15

1.  La contraseña del siguiente nivel se obtiene subiendo la del nivel actual al puerto 30000 en localhost

    cat /etc/bandit_pass/bandit14 | nc localhost 30000


<a id="org5bf166d"></a>

### Contraseña

8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


<a id="org953dabc"></a>

## Level 15 -> 16

1.  De forma similar, se debe subir la contraseña del nivel 15 usando SSL/TLS al puerto 30001

    openssl s_client -crlf -connect localhost:30001 -servername localhost


<a id="orgd75c1b1"></a>

### Contraseña

kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx


<a id="org4dc7d08"></a>

## Level 16 -> 17

1.  Buscar un puerto con un servidor escuchando en el rango de puertos 31000-32000

    nmap -p 31000-32000 localhost

    31046/tcp open  unknown
    31518/tcp open  unknown
    31691/tcp open  unknown
    31790/tcp open  unknown
    31960/tcp open  unknown

1.  Verificar cuál de estos recibe en SSL/TLS

    echo "kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx" | openssl s_client -connect localhost:31790 -ign_eof


<a id="org14a7133"></a>

### Contraseña

    -----BEGIN RSA PRIVATE KEY-----
    MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
    imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
    Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
    DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
    JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
    x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
    KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
    J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
    d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
    YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
    vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
    +TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
    8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
    SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
    HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
    SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
    R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
    Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
    R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
    L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
    blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
    YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
    77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
    dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
    vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
    -----END RSA PRIVATE KEY-----

-   Debe subirse a bandit17

    ssh -i bandit17.key bandit17@bandit.labs.overthewire.org -p 2220


<a id="orga4b6243"></a>

## Level 17 -> 18

1.  Verificar entre dos archivos la línea nueva
    
        diff passwords.old passwords.new 
    
        < BMIOFKM7CRSLI97voLp3TD80NAq5exxk
        ---
        > x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO


<a id="org6c9658f"></a>

### Contraseña

x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO


<a id="org20bcf45"></a>

## Level 18 -> 19

1.  Conectarse al nivel 18 te bota por usar ssh :(
2.  Solo pasar un comando con ssh es necesario
    
        ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme


<a id="orgde73b89"></a>

### Contraseña

cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8


<a id="orgba5def9"></a>

## Level 19 -> 20

1.  La contraseña se encuentra en /etc/bandit<sub>pass</sub>/bandit20
2.  Solo puede leerse con el binario setuid bandit20-do
    
        ./bandit20-do cat /etc/bandit_pass/bandit20


<a id="org4800fb5"></a>

### Contraseña

0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO


<a id="org0c753e2"></a>

## Level 20 -> 21

1.  Debes abrir un servidor en un puerto con netcat, pasarlo al background y usar suconnect
    
        echo -n '0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO' | nc -l -p 1337 &
2.  El comando abrirá un servidor en 1337 que mandará la contraseña al suconnect.
    
        /suconnect 1337

    Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
    Password matches, sending next password
    EeoULMCra2q0dSkYj561DX7s1CpBuOBt


<a id="org1c944dc"></a>

### Contraseña

EeoULMCra2q0dSkYj561DX7s1CpBuOBt

