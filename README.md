# WRO-Future-Engineers-2022-Team-MKS

Als Fahrzeug benutzen wir einen Fischertechnik-Roboter mit TXT 4.0 Controller. Der Code wurde mit der Fischertechnik-Software "ROBO Pro Coding" programmiert. Da leider keine Phython Dokumentation zu diesem Programm und zur Kommunikation mit dem Roboter vorhanden ist mussten wir auf Fischertechnik-Blockly zurückgreifen.
Am Auto ist ein Servomoter (für Lenkung der vorderen Achse), ein Encomotoer (als Antrieb für die Hinterräder), drei Ultraschallsensoren (für die Abstandsmessung), ein Farbsensor (zur FArberkennung der Linien auf der Spielfeldmatte) und mehere Lampen, die aber keinen Einfluss auf die Fahrweise des Auto bringen. Ansonsten besteht das Auto nur aus zusammensteckbaren Fischertechnikteilen.
Das Blockly-Programm wird über W-Lan an den Roboter übertragen und dann direkt ausgeführt.

Der Roboter wurde, durch das von der WRO zur verfügung gestellte "ft Robotics TXT 4.0 Base Set", gebaut. Außderdem haben wir noch das Set "ft Robotics Add On: Autonomous" und ein weiteres Fischertechnik-Standart-Set benutzt. Bei dem Aufbau haben wir uns von dem Add On vorgestellenten Auto inspiriert, haben aber viele verschiedene Sachen verbessert und mehere Sensoren angebracht.

Der Code überprüft permanent, wo der Mittelpunkt des Zwischenraums der beiden Banden ist. Dafür rechnet der Roboter den Abstand der beiden Ultraschallsensoren rechts und links zusammen, dieses Ergebnis teilt er dann durch zwei.
Je weiter weg der Roboter zum Mittelpunkt ist, desto mehr lenkt der Roboter ein, dafür berechnet der Roboter zu wie viel prozent er von dem Mittelpunkt entfernt ist. Hierfür multipliziert er den Wert des Mittelpunkts mit dem Abstandswert der nächsten Bande und dieses Ergebnis teilt er dann durch 100.
Damit die Räder gerade stehen, stellen wir, am Anfang, den Servomoter auf die Position 240. Damit der Servo nicht über den Anschlag der Räder dreht, haben wir festgelegt, dass der Servowert sich maximal 60 von 240 unterscheiden darf. Um jetzt die Lenkung zu berechnen, teilen wir die 60 in 100 Stücke auf. Pro prozent wird dann dieses Stück auf die 240 hinzuaddiert oder subtrahiert. Dadurch lenkt der Roboter, wenn er nah an der Bande ist, sehr stark ein und über die zeit lenkt er dann immer flacher ein, bis er in der Mitte dann wieder auf dem Wert 240 steht.
