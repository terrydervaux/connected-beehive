# Ruche connectée

Ce projet a pour objectif d'aider les apiculteurs à déterminer l'état de santé de leurs ruches à distance.

L'idée est d'utiliser des objets connectés pour réaliser des mesures grâce à des capteurs et de les transmettre à une application mobile. L'application mobile doit permettre à l'apiculteur de consulter les mesures et de configurer des alarmes sur son smartphone afin qu'il soit notifié de l'état de santé de ses ruches en temps réel.

## Composants

| Qte | Nom                             | Usage                                                                                                          | Reference                                                                                                                                                                                                                                             |
| --- | ------------------------------- | -------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Ardouino                        | permet la récupération des signaux, la transformation des signaux en mesure et la transmission des mesures sur un reseau LoRa | Ardouino Uno                                                                                                                                                                                                                                          |
| 1   | Jauge de contrainte             | permet à l'Ardouino de récupérer des signaux correspondant au poids de la ruche                                | Load Cell                                                                                                                                                                                                                                             |
| 1   | Amplificateur                   | permet à l'Ardouino d'amplifier les signaux provenant de la jauge de contrainte                                | HX711 Module                                                                                                                                                                                                                                          |  |
| 1   | Capteur de temperature/humidité | permet à l'Ardouino de récupérer les signaux correspondant à la température et la l'humidité de la ruche       | DHT22                                                                                                                                                                                                                                                 |  |
| 1   | Emetteur/Récepteur LoRa         | permet à l'Ardouino de transmettre les mesures sur un réseau graçe au protocol LoRa                            | [RFM95W LoRa](https://makeradvisor.com/tools/rfm95-lora-transceiver-module/)                                                                                                                                                                          |
| 1   | Antenne                         | permet à l'Ardouino de transmettre les mesures sur plusieurs centaines de mètres                               | [Antenne](https://www.amazon.fr/DollaTek-antenne-connecteur-868-915MHz-Lora32u4/dp/B07QXPN3YR/ref=sr_1_6?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=lora32&qid=1593589548&refinements=p_76%3A437878031&rnid=437877031&rps=1&sr=8-6) |
| 1   | Lora32                          | permet la reception des mesures sur un reseau LoRa et la transmission vers l'application mobile sur un reseau IP connecté à internet                        | [Lora32](https://makeradvisor.com/tools/ttgo-lora32-sx1276-esp32-oled/)                                                                                                                                                                               |

## Librairies

- [Bodge/HX7AA](https://github.com/bogde/HX711/releases/tag/v0.1)

## Sources

- [Tutorial to Interface HX711 Balance Module With Load Cell](https://www.instructables.com/id/How-to-Interface-HX711-Balance-Module-With-Load-Ce/)∏
- [Using 1602 LCD Keypad Shield w/ Arduino](https://create.arduino.cc/projecthub/electropeak/using-1602-lcd-keypad-shield-w-arduino-w-examples-e02d95)
- [ESP32 with LoRa using Arduino IDE – Getting Started](https://randomnerdtutorials.com/esp32-lora-rfm95-transceiver-arduino-ide/)
