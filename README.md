# :bellhop_bell: Challenge-E09: Adressage IP
### François BARSOTTI
## :mag: Pitch de l'exercise
> « Pour les adresses IP et masques de sous-réseau suivants, calculez :
> -	l’adresse de réseau
> -	l’adresse de broadcast
> -	le nombre d’adresses utilisables par des machines
> -	la plage d’adresses disponibles
> Certains utilisent la notation « classique », d’autres la notation CIDR :
>      +	192.168.13.67/24
>      +	172.16.0.1 – 255.255.255.0
>      +	172.16.27.32/23
>      +	10.7.5.1 – 255.255.128.0
>      +	10.42.0.82/12
>        
>Essayez de calculer tout à la main (avec la méthode de votre choix, idéalement essayez d’utiliser les deux !), puis vérifiez vos calculs avec une calculatrice en ligne [exemple](https://www.subnet-calculator.com/cidr.php) ! »
> #
 
Sur la **Méthode du nombre magique**, voici les solutions:
## - Adresses IP: 192.168.13.67/24
- [x] Masque:       255.255.255.0 (on peut reconnaître l'octet significatif comme le premier qui n'est pas 255)
- [x] Nombre magique: 256-0 = 256
- [x] Multiples: 0,256...

Alors,
- [x] Adresse réseau (AR):    192.168.13.0
- [x] Adresse broadcast (AB): 192.168.13.255
- [x] Nombre d'addresses utilisables par des machines:256-2 = 254 car une est réservée pour l'AR et l'autre pour l'AB
- [x] Plage d'adresses disponibles: 192.168.13.1 - 192.168.13.254 (0 sur le dernier octet a été pris par l'AR et 255 sur le dernier octet a été pris par l'AB)
#
- Adresse IP: 172.16.0.1 – 255.255.255.0
- [x] Masque:       255.255.255.0 (on peut reconnaître l'octet significatif comme le premier qui n'est pas 255)
- [x] Nombre magique: 256-0 = 256
- [x] Multiples: 0,256...
Alors,
- [x] Adresse réseau (AR):    172.16.0.0 
- [x] Adresse broadcast (AB): 172.16.0.255
- [x] Nombre d'addresses utilisables par des machines:256-2 = 254 car une est réservée pour l'AR et l'autre pour l'AB
- [x] Plage d'adresses disponibles: 172.16.0.1 - 172.16.0.254 (0 sur le dernier octet a été pris par l'AR et 255 sur le dernier octet a été pris par l'AB)
#
- Adresses IP: 172.16.27.32/23
- [x] Masque:       255.255.254.0 (en sachant qu'en binaire le "1111 1110" du troisième octet = 254)
- [x] Nombre magique: 256-254 = 2
- [x] Multiples: 0,2,4,6,...,26,28,30...
Alors,
- [x] Adresse réseau (AR):    172.16.26.0
- [x] Adresse broadcast (AB): 172.16.27.255
- [x] Nombre d'addresses utilisables par des machines:256-2 = 254 car une est réservée pour l'AR et l'autre pour l'AB
- [x] Plage d'adresses disponibles: 172.16.26.1 - 172.16.27.254 (0 sur le dernier octet a été pris par l'AR et 255 sur le dernier octet a été pris par l'AB)
#
- Adresses IP: 10.7.5.1 (Classe A ou < 126)
- [x] Masque:       255.0.0.0 (par défaut pour les IP de Classe A, car il y a 24 bits libres pour les hôtes)
- [x] Nombre magique: 256-0 = 256
- [x] Multiples: 0,2,4,6,...,256...
Alors,
- [x] Adresse réseau (AR):    10.0.0.0
- [x] Adresse broadcast (AB): 10.255.255.255
- [x] Nombre d'addresses utilisables par des machines:256-2 = 254 car une est réservée pour l'AR et l'autre pour l'AB
- [x] Plage d'adresses disponibles: 10.0.0.1 - 10.255.255.254 (0 sur le dernier octet a été pris par l'AR et 255 sur le dernier octet a été pris par l'AB)
#
- Adresses IP : 10.42.0.82/12 (encore Classe A ou < 126)
- [x] Masque:       255.0.0.0 (par défaut pour les IP de Classe A, car il y a 24 bits libres pour les hôtes)
- [x] Nombre magique: 256-0 = 256
- [x] Multiples: 0,2,4,6,...,256...
Alors,
- [x] Adresse réseau (AR):    10.0.0.0
- [x] Adresse broadcast (AB): 10.255.255.255
- [x] Nombre d'addresses utilisables par des machines:256-2 = 254 car une est réservée pour l'AR et l'autre pour l'AB
- [x] Plage d'adresses disponibles: 10.0.0.1 - 10.255.255.254 (0 sur le dernier octet a été pris par l'AR et 255 sur le dernier octet a été pris par l'AB)
##
Sur la **Méthode ET/OU logique** je n'arrive pas à tout résoudre, mais uniquement faire la conversion décimal/binaire du Masque:
- Adresses IP : 192.168.13.67/24
- [x] Masque décimal:    255.      255.      255.       0
- [x] Masque binaire: 1111 1111.1111 1111.1111 1111.0000 0000
#
- Adresses IP : 172.16.0.1
- [x] Masque décimal:    255.      255.      255.       0
- [x] Masque binaire: 1111 1111.1111 1111.1111 1111.0000 0000
#
- Adresses IP : 172.16.27.32/23
- [x] Masque décimal:    255.      255.      254.       0
- [x] Masque binaire: 1111 1111.1111 1111.1111 1110.0000 0000
#
- Adresses IP : 10.42.0.82 – 255.255.128.0
- [x] Masque décimal:    255.       0.        0.        0
- [x] Masque binaire: 1111 1111.0000 0000.0000 0000.0000 0000
#
- Adresses IP : 10.42.0.82/12
- [x] Masque décimal:    255.       0.        0.        0
- [x] Masque binaire: 1111 1111.0000 0000.0000 0000.0000 0000

