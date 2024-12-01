[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/ULiw8LbN)

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



Ex 2 part 3

1- Fent servir la configuració per defecte del mòdul logging: Exemple: python logging.basicConfig(level=logging.INFO) logging.info("Missatge per defecte").
Avantatges:  -Configuració ràpida i fàcil 
- No cal gaire codi.
Desventatges: - No és flexible: només permet configuracions bàsiques.
- No es poden gestionar múltiples logs complexos.

2- Instanciant un objecte logger i parametrizant-lo des del programa: Exemple: python logger = logging.getLogger("my_logger") handler = logging.StreamHandler() logger.addHandler(handler) logger.warning("Advertència")
Avantatges: - Major flexibilitat per personalitzar el logger.
- Es poden afegir múltiples handlers per diferents sortides (pantalla, fitxer, etc.)
Desventatges: - La configuració pot ser més llarga i complexa.
- És necessari més codi per a la configuració inicial.

3- Instanciant un objecte logger a partir d'una configuració emmagatzemada a fitxer: Exemple: python import logging.config logging.config.fileConfig("logging.conf") logger = logging.getLogger("exampleLogger") logger.error("Missatge d'error")
Avantatges: - Configuració avançada i reutilitzable.
- Es pot modificar fàcilment sense canviar el codi Python.
  Desventatges: - Es necessita mantenir un fitxer extern (fitxer de configuració).
- Pot ser complicat per a configuracions senzilles.


Ex 2 part 4
Cerca llibreries de logs en altres llenguatjes (al menys 2, i identifica cóm resolen les següents característiques típiques d’un sistema de logging.  Omple la següent taula, i inclou-la al read-me del repositori:

-Llenguatge: java
-Nom de la llibreria: Log4j
-És nativa del llenguatge? No
-URL per descarregar-se la llibreria: https://logging.apache.org/log4j/2.x/
-Inicialització de l'objecte de logger: Logger logger = LogManager.getLogger(YourClass.class);
-Nivells de log disponibles: TRACE, DEBUG, INFO, WARN, ERROR, FATAL
-Mètode per fer log: logger.info("Missatge d'informació");
-Tipus de manejadors (pantalla, fitxer...) Identificar els seus noms a l'API: ConsoleAppender, FileAppender
-Opcions de format: Es pot definir un patró (PatternLayout) com %d %p %c{1.} [%t] %m%n per mostrar data, nivell, etc.


-Llenguatge: JavaScript
-Nom de la llibreria: Winston
-És nativa del llenguatge? No
-URL per descarregar-se la llibreria: https://www.npmjs.com/package/winston	
-Inicialització de l'objecte de logger: const logger = require('winston');
-Nivells de log disponibles: error, warn, info, http, verbose, debug, silly
-Mètode per fer log: logger.info("Missatge d'informació");
-Tipus de manejadors (pantalla, fitxer...) Identificar els seus noms a l'API: Console Transport, File Transport
-Opcions de format: Winston utilitza format.combine() per definir formats amb opcions com timestamp() i printf().




Ex 3
Mitjançant les eines proposades a continuació, voldríem elaborar una petita aplicació que permetés a un treballador de forma senzilla introduir mitjançant un fitxer json, txt csv o similar introduir unes dades que escollim i li elaborem una sèrie de gràfiques.

Abans d’això, caldrà informar-se sobre les següents eines, alguna de les quals potser ja coneixeu.
Pandas
Jupyter Notebook
reportlab
La idea d'aquest punt és detallar,

-1.La funcionalitat de cada una de les eines presentades.
Pandas: Permet llegir dades de diferents tipus de fitxers, com ara CSV, JSON, Excel, entre d'altres, convertint-los fàcilment en DataFrames per a la seva anàlisi.

Jupyter: Permet executar codi Python i veure els resultats immediatament. A més, permet afegir comentaris i anotacions, la qual cosa fa que el procés sigui molt visual i permet crear i visualitzar gràfiques.

Reportlab: Permet generar documents PDF amb text, gràfiques, taules i altres elements de formatació.

-2.Caldrà posar captures de les proves que heu fet i argumentar quines eines i llibreries utilitzareu finalment.
A projecte hem començat a tocar aquestes eines on amb creem un DataFrame amb Pandas, generem una gràfica bàsica amb matplotlib dins de Jupyter Notebook, i després guardar-la en un PDF amb reportlab.
Et deixo al rar l'activitat de projecte on ho vem tocar. Anomenat Ex3P2


Exercici 7
-Un informe de la part de logging amb el codi que s’ha utilitzat i els exemples d’utilització i resultats.

Logging permet el seguiment del comportament del sistema, documentar esdeveniments i detectar problemes durant l'execució del programa.
En aquest projecte, s'ha utilitzat la llibreria de logging de Python per monitoritzar el procés de càrrega de dades i anàlisi.

Explicació del exemple a ExercicisPart2:
La funció logging.basicConfig() configura el format del missatge i el nivell del logging (INFO en aquest cas).
logging.info() s'ha utilitzat per registrar èxits (per exemple, la correcta càrrega del CSV).
logging.warning() per registrar possibles problemes que no bloquegen el programa (per exemple, dades nul·les).
logging.error() per registrar errors que necessiten una acció immediata.


-Un informe de la part del tractament de dades, que s’expliqui cada part que s’ha
utilitzat així com les gràfiques que es mostren.

L'objectiu principal era analitzar les notes dels alumnes en diferents mòduls i obtenir resultats significatius sobre el rendiment general.
Les dades es van bolcar des d'un fitxer CSV i es van analitzar utilitzant Pandas.


