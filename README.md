# WRO-Future-Engineers-2022-Team-MKS

Als Fahrzeug benutzen wir einen Fischertechnik-Roboter mit TXT 4.0 Controller. Der Code wurde mit der Fischertechnik-Software "ROBO Pro Coding" programmiert. Da leider keine Phython Dokumentation zu diesem Programm und zur Kommunikation mit dem Roboter vorhanden ist mussten wir auf Fischertechnik-Blockly zurückgreifen.
Am Auto ist ein Servomoter (für Lenkung der vorderen Achse), ein Encomotoer (als Antrieb für die Hinterräder), drei Ultraschallsensoren (für die Abstandsmessung), ein Farbsensor (zur FArberkennung der Linien auf der Spielfeldmatte) und mehere Lampen, die aber keinen Einfluss auf die Fahrweise des Auto bringen. Ansonsten besteht das Auto nur aus zusammensteckbaren Fischertechnikteilen.
Das Blockly-Programm wird über W-Lan an den Roboter übertragen und dann direkt ausgeführt.

Der Roboter wurde, durch das von der WRO zur verfügung gestellte "ft Robotics TXT 4.0 Base Set", gebaut. Außderdem haben wir noch das Set "ft Robotics Add On: Autonomous" und ein weiteres Fischertechnik-Standart-Set benutzt. Bei dem Aufbau haben wir uns von dem Add On vorgestellenten Auto inspiriert, haben aber viele verschiedene Sachen verbessert und mehere Sensoren angebracht.

Der Code überprüft permanent, wo der Mittelpunkt des Zwischenraums der beiden Banden ist. Dafür rechnet der Roboter den Abstand der beiden Ultraschallsensoren rechts und links zusammen, dieses Ergebnis teilt er dann durch zwei.
Je weiter weg der Roboter zum Mittelpunkt ist, desto mehr lenkt der Roboter ein, dafür berechnet der Roboter zu wie viel prozent er von dem Mittelpunkt entfernt ist. Hierfür multipliziert er den Wert des Mittelpunkts mit dem Abstandswert der nächsten Bande und dieses Ergebnis teilt er dann durch 100.
Damit die Räder gerade stehen, stellen wir, am Anfang, den Servomoter auf die Position 240. Damit der Servo nicht über den Anschlag der Räder dreht, haben wir festgelegt, dass der Servowert sich maximal 60 von 240 unterscheiden darf. Um jetzt die Lenkung zu berechnen, teilen wir die 60 in 100 Stücke auf. Pro prozent wird dann dieses Stück auf die 240 hinzuaddiert oder subtrahiert. Dadurch lenkt der Roboter, wenn er nah an der Bande ist, sehr stark ein und über die zeit lenkt er dann immer flacher ein, bis er in der Mitte dann wieder auf dem Wert 240 steht.

![Bildschirmfoto 2022-06-23 um 19 54 22](https://user-images.githubusercontent.com/80636354/175364561-4b3d1245-0b31-495b-92c5-4162f39c649d.png)


Video: https://youtu.be/jOzxhZ0cUeA



![D5FC61FD-75B5-4141-97F4-84528C915262](https://user-images.githubusercontent.com/92917467/175514876-885f22a0-c331-491a-91dd-b67cf4c7bdbe.jpeg)
![62EA49C4-36FE-45A9-9CEE-321A4FDE42DF](https://user-images.githubusercontent.com/92917467/175514881-4ead435c-84a9-49dd-9f2d-f02f1950d4f8.jpeg)
![5005F555-C3C0-445C-AEA9-E11F4901D836](https://user-images.githubusercontent.com/92917467/175514882-a3e38f40-7f8d-4a4a-9bc2-7d3f011a4fc8.jpeg)
![3934B7E1-405D-47DC-9ED7-087BA8643719](https://user-images.githubusercontent.com/92917467/175514885-bae152b3-fae3-4526-8824-b0dc68f63e7f.jpeg)
![8452BA58-0B8F-41A1-B4FF-2FE174755D2C](https://user-images.githubusercontent.com/92917467/175514892-d0a1d54d-039e-4c54-8ed2-b9ad460fe42e.jpeg)
![4D22F299-205C-464F-B322-CE2C94EB3943](https://user-images.githubusercontent.com/92917467/175514895-c6d14799-1146-418c-9039-f18a5bebefbd.jpeg)


[Schaltplan-TeamMKS.pdf](https://github.com/NickTechMaster/WRO-Future-Engineers-2022-Team-MKS/files/8975653/Schaltplan-TeamMKS.pdf)

