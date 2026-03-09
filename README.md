\# Oscilador Astable con Temporizador 555



\## 1. Introducción



En este proyecto se diseñó e implementó un circuito oscilador astable utilizando el circuito integrado NE555. El objetivo fue generar una señal periódica capaz de encender y apagar un LED de forma continua, permitiendo observar el comportamiento de una señal cuadrada en un circuito electrónico básico.



El sistema utiliza una fuente de 9V regulada a 5V mediante un regulador de voltaje LM7805 para alimentar de forma estable el temporizador 555.



---



\## 2. Objetivo



Diseñar y montar un circuito oscilador astable que genere una señal periódica utilizando el temporizador 555, permitiendo visualizar la oscilación mediante un LED.



---



\## 3. Componentes utilizados



\* 1 × NE555 (temporizador)

\* 1 × LM7805 (regulador de voltaje)

\* 1 × batería de 9V

\* 1 × capacitor electrolítico de 10 µF

\* 1 × capacitor electrolítico de 100 µF

\* 1 × resistencia de 10 kΩ

\* 1 × resistencia de 68 kΩ

\* 1 × resistencia de 220 Ω (para el LED)

\* 1 × LED

\* Protoboard

\* Cables de conexión



---



\## 4. Regulación de voltaje



La batería de 9V se conectó al regulador LM7805 para obtener una salida estable de 5V.



Conexiones del regulador:



\* IN → positivo de la batería (9V)

\* GND → tierra del circuito

\* OUT → línea de alimentación de 5V



Se utilizó un capacitor de 100 µF entre OUT y GND para estabilizar el voltaje.



---



\## 5. Configuración del temporizador 555 (modo astable)



El temporizador 555 fue configurado en modo astable para generar una señal periódica continua.



Conexiones principales:



\* Pin 1 → Tierra

\* Pin 8 → 5V

\* Pin 4 → 5V

\* Pin 2 y Pin 6 → conectados entre sí

\* Pin 7 → conectado entre las resistencias

\* Pin 3 → salida del circuito



---



\## 6. Red RC del oscilador



La frecuencia de oscilación se determinó utilizando dos resistencias y un capacitor.



R1 = 10 kΩ

R2 = 68 kΩ

C = 10 µF



Conexiones:



\* R1 entre pin 8 y pin 7

\* R2 entre pin 7 y pin 2-6

\* Capacitor de 10 µF entre pin 2-6 y tierra



---



\## 7. Salida del circuito



La señal de salida se obtiene del pin 3 del temporizador 555.



Para visualizar la oscilación se conectó un LED con una resistencia limitadora:



Pin 3 → resistencia de 220 Ω → LED → tierra



Esto permite que el LED encienda y apague de manera periódica.



---



\## 8. Funcionamiento del circuito



El capacitor se carga a través de las resistencias R1 y R2 hasta alcanzar aproximadamente 2/3 del voltaje de alimentación. En ese momento, el temporizador cambia de estado y el capacitor comienza a descargarse a través de R2.



Cuando el voltaje del capacitor cae por debajo de 1/3 del voltaje de alimentación, el temporizador vuelve a cambiar de estado, reiniciando el ciclo.



Este proceso se repite continuamente generando una señal cuadrada en la salida del pin 3.



---



\## 9. Frecuencia de oscilación



La frecuencia de la señal se calcula mediante la ecuación:



f = 1.44 / ((R1 + 2R2) C)



Sustituyendo los valores utilizados en el circuito:



R1 = 10kΩ

R2 = 68kΩ

C = 10µF



El resultado produce una frecuencia aproximada cercana a 1 Hz, lo que permite observar el parpadeo del LED de manera clara.



---



\## 10. Conclusión



El circuito implementado demuestra el funcionamiento del temporizador 555 en configuración astable. Mediante el uso de una red RC se logra generar una señal periódica estable que puede ser observada fácilmente mediante un LED.



Este tipo de circuito es ampliamente utilizado en aplicaciones como generadores de pulsos, temporizadores, moduladores y sistemas de control digital.



