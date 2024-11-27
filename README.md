[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/ULiw8LbN)
# Empty
Exercici 1
Explica quines comandes de Linux Pots fer servir a l’hora d’analitzar logs escrits a fitxer per a:

1.1 Veure contínuament els logs que es van escrivint a un arxiu
Per veure els log que es van afegint, utilitzarem tail -f
    -tail -f logs.log
Per veure nomes les 7 ultimes linies utilitzarem tail -n
 -tail -n 7 -f logs.log

1.2 Cercar una paraula concreta dintre d’un arxiu de log
Per buscar una paraula en concret utilitzarem la comanda grep
    -grep "error" logs.log
Per ignorar majuscules i minuscules utilitzarem grep -i
    -grep -i "error" logs.log


Ex 2 part 2
Que creieu que és millor mostrar els logs per exemple a la terminal durant l'execució del programa o bolcar-los en un fitxer de text?
Jo crec que en cas de que estiguis desenvolupant un petit projecte veure els logs a la terminal es una bona idea i molt pràctic ja que tels mostra inmediatament, pero en cas de que el teu projecte sigui molt ampli si t'anira millor tindre l'historial dels logs guardat en una carpeta aixi ho pots consultar en cualsevol moment.

