#Logboek WarDrive
## Week 4/07/2016 - 10/07/2016
Geprobeert om Debian te installeren op een oude laptop omdat ik eerst een raspberry pi wou gebruiken maar heb deze niet ter beschikking dus wou ik iets zo dicht mogelijk bij dezelfde werking blijven van Raspberry Jessie. Maar om 1 of andere manier werkte debian niet goed in de installatie dus heb ik Kali geprobeert dit werkte wel met succes en konden we op zoek naar een Bluetooth module omdat ik de gps van mijn gsm ga gebruiken maar deze methode heeft een bluetooth module nodig omdat mijn laptop geen bluetooth heeft ingebouwd. Laten we het erbij houden dat deze niet meer geinstalleerd is. Dus ik hoop dat ik deze snel te pakken kan krijgen.

## Week 18/07/2016 - 24/07/2016
Toch een raspberry PI gekocht om gemakkelijker te kunnen werken met een gps module die ik dan geleend heb.

## Week 25/07/2016 – 31/07/2016
Gestart met het installeren van de Raspbian Jessie op de Raspberry pi. Deze iso moet dan via Win32Disk bootable stick van gemaakt worden. Wat dan uiteindelijk geen stick is maar een SD kaartje. Zodra Raspbian jessie is geinstalleer kunnen we de juiste stappen gaan volgen om de opdracht op de juiste manier te kunnen uitvoeren.

## Week 1/08/2016 – 7/08/2016	

Ik heb een goede Wardrive tutorial gevonden die werkt met Kismet dus ben ik deze Tutorial gaan volgen. De eerste stap was om het me gemakkelijker te maken dat ik niet steeds een toetsenbord, scherm en muis nodig had maar enkel voeding. Dus ben ik ssh gaan instellen hiervoor moet natuurlijk wel nog eerst een scherm en toestenbord gebruikt worden maar nadien kunnen we gewoon via putty naar het juiste ip address van de pi, dat we dan aansluiten op het netwerk met een ethernet kabel, verbinden. Vanaf dit in orde was en werkte kunnen we de installatie doen die we nodig hebben om de opdracht te vervolledigen. 
Daarna kunnen we gewoon op de laptop verder en werken via putty wat het ook makkelijker maakt om sneller te kunnen op zoeken als er iets fout gaat. Nu kunnen we verder met het installeren van GSPD dit is eigenlijk optioneel maar maakt ons wel beter om te kunnen controleren of de gps module zeker werkt en ook ofdat de gps module wel degelijk een juiste gps locatie weergeeft. 
Eerst moeten we de juiste commando’s ingeven voor het installeren van de juiste software en daarna moeten we dan controleren of de GPS module herkent is door de pi zelf door lsusb te doen wat we ook in verder commando’s gaan nodig hebben. 
Na alles geinstalleerd te hebben en juist geconfigureerd kunnen we nu de gps locatie checken en kunnen we zien waar op de wereld we ons bevinden.

##Week 8/08/2016 – 14/08/2016
Nu kunnen we verder met het installeren en juist configureren van Kismet. Eerst moeten we dan een zipke downloaden die we later moeten uitpakken en zo de installatie kunnen voltooien. Dit installeren heeft wel een paar uur gekost. Daarna konden we de juiste configuraties uitvoeren zoals de ncsource gelijk stellen aan wlan0 maar ook de gps op true zetten en het gpstype op gpsd en ook op serial zetten en dan linken aan de juiste usb poort waarop de gps module is ingestoken.

## Week 15/08/2016 – 21/08/2016
De volgende stappen waren om Kismet te starten en te testen. We kunnen kismet manueel starten maar we kunnen dit ook  automatisch een server laten opstarten zodra we de Raspberry pi opstarten. Maar om 1 of andere reden is dit niet gelukt en wou hij deze server nooit opstarten van in het begin. Maar ik zelf vond dit niet echt een groot probleem omdat het manueel opstarten ook niet heel lang duurt. Daarna ben ik beginnen nadenken dat ik een oplossing moet zoeken voor ssh te kunnen laten werken als ik geen wifi heb van thuis tijdens het rondrijden. Daarbij kwam ik dan uit om een direct netwerkconnectie met de pi uit te voeren. Waarbij de laptop automatisch zijn ip moet krijgen en de pi een prive address krijg van 169.254.0.2 waarmee ik dan met dit adress via putty kan ssh’en.
Dus we kunnen overgaan tot het testen van Kismet in samenwerking met de wifi module en de gps module. Dus ben ik gaan rondrijden.  Na het rondrijden en het detecteren van netwerken kunnen we de server afsluiten en wordt er een file aangemaakt in .netxml. deze file moeten we dan omzetten naar een kml file via een scriptje dat we kunnen downloaden van internet. Dit scriptje zet dan de .netxml file om in een kml en kmz file. De kml file kunnen we dan gebruiken om in google maps te plaatsen zodat we een mooi overzicht hebben van de verschillende acces punten die ik op mijn route ben tegengekomen.
