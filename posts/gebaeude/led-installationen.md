<!--
.. title: LED-Installationen
.. slug: led-installationen
.. date: 2019-11-24 21:12:19 UTC+01:00
.. tags: led, gebauede 
.. category: gebauede, led
.. link: 
.. description: Wikiseite zu den LED Installationen im Toolbox Gebäude 
.. type: text
.. author: Jonas Otto
-->

 LED-Installationen in der Toolbox

In der Toolbox sind und sollen verschiedene LED-Installationen das Haus verschönern. Auf dieser Wikiseite sollen ein paar Informationen und hilfreiche Tipps, so wie Ansprechpartner für Debugging usw. gesammelt werden.

**LED-Installationsorte:**

  * Treppenmatrix
  * Besprechungsraum
  * LED-Tunnel und -Ring über der Treppe


 Ansteuerung
----------

Mehrere Leute beschäftigen sich in der Toolbox mit der wichtigen Problemstellung, wie man am besten VIELE NeoPixel-artige (individuell ansteuerbare) RGB-LED-Streifen (zentral) ansteuert. Kr0l macht da was mit ARTnet, Jonas (ottojo) baut immer mal wieder an WiFi-basierten Lösungen mit dem ESP8266 und hat da auch mal [Platinen](https://github.com/ottojo/wifiblink) bestellt.

 Treppenmatrix
-----------------

![LED-Treppe](/galleries/led-treppe.jpg "LED Treppe")
Die Treppenmatrix ist die Treppe am Eingang hoch ins erste Stockwerk. 17 Treppenstufen sind hier mit LEDs an den Schwellen ausgestattet, so dass sich eine Matrix bildet. Die LED-Ketten sind jeweils noch mit einem Tuch vorne verdeckt, damit sie möglichst wenig blenden, wenn man von unten die Treppe Hinaufläuft.

|Verbaute LEDs  | Meter | LEDs pro Meter | LED Typ | Netzgerät | Controller | Fertig?|
| --- | --- | --- | --- | --- | --- | --- |
|612  |20,4  |30  |WS2811  |12V, 3A|ESP8266|  Nein|


(Matrix: Breite 11, Höhe 17)

**Steuerung**

Die Steuerung übernimmt derzeit ein ESP8266, der in einem Holzkästchen am oberen Anfang der Treppe angebracht ist. Am Kästchen außen sind zwei Taster und ein Schalter angebracht, die zur Steuerung dienen. Die Software ist auf [github.com/ToolboxBodensee/fastLED-Treppe](https://github.com/ToolboxBodensee/fastLED-Treppe) zu finden. Sie basiert auf der NeoPixelBus Library. Der Schalter schaltet die LEDs an/aus, die Taster wechseln zwischen verschiedenen Animationen.
Der Code kann über ArduinoOTA updated werden.

**Zukunftsplan**

Der Plan für die Zukunft ist erst einmal das Steuerungskästchen fertigzumachen, also die Knöpfe in die Steuerung einzubeziehen und ein paar wechselnde Animationen zu erstellen. Später soll die Treppe via ARTnet in die hoffentlich irgendwann einmal kommende Lichthaussteuerung eingebaut werden, mit Webinterface usw.

 Besprechungsraum
-------------------

Im Besprechungsraum gibt es zwei LED-Installationen. Die eine befindet sich an der Decke und kann an der Tür mit einem Schalter aktiviert werden, die andere auf dem Tisch, diese ist jedoch noch nicht sonderlich weit ausgebaut.

 Decke
---------
Die Installation an der Decke kann mit dem Schalter an der Tür an- und ausgeschaltet werden.

| Verbaute LEDs | Meter | LEDs pro Meter | LED Typ | Netzgerät | Controller | Fertig?|
| --- | --- | --- | --- | --- | --- | --- |
|ca 450  |ca 15  |30  |WS2811  |12V, 3A|Arduino UNO|  Nein|

**Steuerung**

Als Steuerplatine dient auch hier derzeit ein Arduino UNO mit der FastLED Libary. Die Deckeninstallation kann derzeit einfach nur an- und ausgeschaltet werden, worauf ein indirekter LED-Streifen an der Decke seine Funktion aufnimmt. Bei der Tischinstallation soll ein ähnliches Schema angewendet werden.

Der Code ist auf [GitHub](https://github.com/ToolboxBodensee/ruum42LEDs).

**Zukunftsplan**

Auch hier ist wieder die Idee, die LEDs mit in die hoffentlich kommende Lichthaussteuerung aufzunehmen. Also wie gehabt, ARTnet Controller usw…

 Tisch
---------

WS2811-Streifen mit 3 RGB-LEDs pro Pixel sind rund um das Steckdosen-LAN-Fiber-Anschluss-Ding (TODO: Namen herausfinden) angebracht. Unter dem Tisch hängt ein ESP8266 mit Shield für Levelshifting, an den die LEDs angeschlossen sind.
Auf dem ESP läuft [github.com/toblum/McLighting](https://github.com/toblum/McLighting.git) .

 Ansteuerung
------------
Auf [r42-led.tbbs.me](http://r42-led.tbbs.me) können die LEDs bedient werden.

| Verbaute LEDs  | Meter | LEDs pro Meter  | LED Typ  | Netzgerät  | Controller  | Fertig?|
| --- | --- | --- | --- | --- | --- | --- |
|idk  |9|10 Pixel mit je 3 RGB Leds|WS2811|  12V, 6A  |  ESP8266  |  Nein  |

\\

