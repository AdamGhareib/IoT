# Stel de LED strip kleur via een colorpicker in via Adafruit IO

Gemaakt door Adam el Ghareib - 500849066
5 oktober 2022

# Introductie

In deze tutorial ga je leren hoe je de kleur van je LED strip aanroept via een colorpicker van Adafruit IO.

Adafruit IO is een Internet of Things platform waar je (gebruik makend van het MQTT protocol) sensordata online zichtbaar kunt maken in een zogenaamde “feed”, en waar je je actuatoren via het web (desktop of mobiel) kunt bedienen. 

# Benodigde hardware componenten

- 1x Arduino Board (ESP8266 Development Board)
- 1x LED strip

# Stap 1: Installeer de Arduino IO libraries

Om de communicatie met Adafruit IO tot stand te kunnen brengen, moeten we wat extra libraries installeren met behulp van de Arduino 

1. Klik op de 3e tab (zie onderstaande afbeelding) 
2. zoek naar  Adafruit IO Arduino (by Adafruit) in in het zoekvak,
3. Install (kies Install All)
<img src="/images/InstallLibrary.png" width="375px">

# Stap 2: Adafruit IO Setup

Om gebruik te kunnen maken van Adafruit IO, moeten we eerst een account en een dashboard aanmaken. 

1. Ga daarvoor naar https://io.adafruit.com/ , klik op “Get Started for Free” en maak een account aan.  
2. In Adafruit IO: ga de gele sleutel in het menu
<img src="/images/ActivateKey.png">
3. Kopieer je key en username

# Stap 3: Adafruit IO Feed en Colorpicker aanmaken

In adafruit IO

1. Dashboards > New Dashboard (Maak een dashboard aan)
2. Ga naar het dashboard
3. Create New Block  via:
<img src="/images/Settings.png" width="375px" alt="settings">
4. Kies color Picker
5. Create de feed name: color
6. Create Block
7. Stel een kleur in met de Color Picker

# Stap 4: Code aanpassen

1. In Arduino: File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel
2. In tab ‘config.h’: plak je Adafruit IO username en Key in
3. In tab ‘config.h’: voer het wifi netwerk en wachtwoord in 
4. (De NodeMCU werkt niet op 5Ghz WiFi)
5. Gebruik liefst de hotspot van je telefoon, dit gebruikt < 0.1 Mb data per uur, dus niet bang zijn
6. in de Tab adafruit_14_Neopixel.ino
7. Pas: #define **PIXEL_PIN 5** aan naar #define **PIXEL_PIN D5**

# Stap 5: Code uploaden (of druk eerst op het vinkje =  Verify)

1. Upload de code
2. Activeer de ‘Serial Monitor’ 
3. Open de serial monitor (tab onderaan)
4. Zet de serial monitor op 115200 baud
<img src="/images/Baud.png">
5. Als alles gelukt is zie je in de serial monitor dat je verbonden bent 
6. Verander nu in Adafruit IO de kleur, dat zie je terug in de Serial monitor
7. Is je ledstrip ook goed aangesloten, dan kun je met de colorpicker de LED kleur aanpassen. Je hebt dus zelf een Philips (Signify) HUE gemaakt. Voor een paar euro. Adafruit draait ook op je mobiel, dus kun je nu (bijna) alles in het filmpje van Les1 

# Errors:

Probleem:
<img src="/images/Error1.png">
<img src="/images/Error2.jpeg">

Oplossing:
<img src="/kjhuimages/Error3.png">

# Bronnen:

https://docs.google.com/document/d/14jhaxaJUhuu0p6_u_oNj8_50Y6PAmtrvcePtKc0HDGs/edit#
