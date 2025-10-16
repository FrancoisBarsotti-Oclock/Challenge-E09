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
 - Adresses IP : 192.168.13.67/24

Sur la **Méthode du nombre magique**, voici la solution:
Adresses IP : 192.168.13.67/24
- [x] Masque:       255.255.255.0 (on peut reconnaître l'octet significatif comme le premier qui n'est pas 255)
- [x] Nombre magique: 256-0 = 256
- [x] Multiples: 0,256...

Alors,
- [x] Adresse réseau (AR):    192.168.13.0
- [x] Adresse broadcast (AB): 192.168.13.255
- [x] Nombre d'addresses utilisables par des machines:256-2 = 254 car une est réservée pour l'AR et l'autre pour l'AB
- [x] Plage d'adresses disponibles: 192.168.13.1 - 192.168.13.254 (0 sur le dernier octet a été pris par l'AR et 255 sur le dernier octet a été pris par l'AB)

