This is the user-friendly beginner Python project that teaches Solar System facts.
This was created to teach my wards in grades 5 and 7.
So far, I'm trying to combine educative programs while learning to write code.




import os

#Set USB path (adjust if needed)

#Planet data
planets = { 
    "Mercury": { 
        "Description": "Closet palnet to the sun. Small, rocky.",
        "Moons": 0,
        "Revolution": "88 Earth days",
        "Rotation": "59 Earth days (prograde, like the Earth ie anticlockwise)",
        "Diameter": "4,880 km",
        "Supports Life": "No",
        "Discovery": "Known since ancient times (Prehistoric observations) by Greeks, Mayans, Babylonians. Visble to the naked eye, but first studied by Mriner 10 Spacecraft in 1974-75",
        "Distance from the sun": "57.9 million km (0.39 AU)"
    },
    "Venus": {
        "Description": "Hottest planet, rocky with volcanic plains and thick Carbon dioxide(CO2) atmosphere.",
        "Moons": 0,
        "Revolution": "225 Earth days",
        "Rotation": "243 Earth days (retrograde ie clockwise so the sun rises in the West and sets in the East )",
        "Diameter": "12.104 km",
        "Supports Life": "No",
        "Dicovery": "Known since ancient times(Prehistoric observations) by Greeks, Babylonians, Mayans. Bightest object in the the sky after the Moon; detailed mapping by Magellan spacecraftin 1990s",
        "Distance from the sun": "108.2 million km (0.72 AU)"

    },
    "Earth": {
        "Description": "Our home planet, silcate crust, oceans and continents.",
        "Moons": 1,
        "Revolution": "365 days",
        "Rotation": "24 hours (prograde)",
        "Diameter": "12,742 km",
        "Supports Life": "Yes",
        "Discovery": "NA, Studied since ancient times: modern understanding from satelites and space misions 1960-70s",
        'Distance from the sun': "149.6 million km (1 AU)"
    },
    "Mars": {
        "Description": "The Red Planet with a thin atmosphere, iron oxide soil.",
        "Moons": 2,
        "Revolution": "687 Earth days",
        "Rotation": "24.6 hours (prograde, like Earth)",
        "Diameter": "6,779 km",
        "Supports Life": "no (but may have supported life in the past)",
        "Description": "Known since ancient times ; studied by Mariner 4 (1965)",
    },
    "Jupiter": {
        "Description": "Largest planet, gas giant with thick atmosphere and GreatRedSpot storm.",
        "Moons": 95,
        "Revolution": "12 Earth years",
        "Rotation": "10 hours (fastest rotation, prograde)",
        "Diameter": "139,820 km",
        "Support Life": "No (but moon like Europa may)",
        "Discovered": "Known since ancient times; Galileo discovered its 4 large moons (Io, Europa, Ganymede, Callisto) in 1610",
        "Distance from the sun": "778.5 million km (5.2 AU)"

    },
    "Saturn": {
        "Description": "Gas giant famous for its Rings made of ice and rocks",
        "Moons": 146,
        "Revolution": "29 Earth years",
        "Rotation": "10.7 hours (prograde)",
        "Diameter": "116,460 km",
        "Supports Life": "No (Titan moon may support conditions for life)",
        "Discovery": "Known since ancient times; rings first observerd by Galileo in 1610",
        "Distance from the sun": "1.43 billion km (9.58 AU)"
    },
    "Uranus": {
        "Description": "an ice giant with methane atmosphere, tilted on its side (98D)",
        "Moons": 27,
        "Revolution": "84 Earth years",
        "Rotation": "17 hours (retrograde)",
        "Diameter": "50,734 km",
        "Supports Life": "No",
        "Discovery": "William Herschell in 1781, first planet found with a telescope",
        "Distance from the sun": "2.87 billion km (19.22 AU)"
    },
    "Neptune": {
        "Description": "Ice giant with supersonic winds and methane-rich atmophere.",
        "Moons": 14,
        "Revolution": "165 Earth years",
        "Rotation": "16 hours (prograde)",
        "Diameter": "49,244 km", 
        "Supports Life": "No",
        "Discovered": "1846 by JonhsonGaile & Heinrich d'Arrest, based on Urbain Le Verrier's calcultions",
        "Distance from the sun": "4.5 billion km (30.05 AU)"

    }   
       
}


usbPath = "/media/snow/USB DRIVE/worldPlanetsQuiz.txt"

with open(usbPath, "w", encoding="utf-8") as f:
    header = f"\n===CORNELIUS-SNOWHYT'S SOLAR SYSTEM NOTES===\n\n"
    print(header)
    f.write(header)

    for i, (planet, info) in enumerate(planets.items(), start=1):
        output = f"{i}. {planet}\n"
        for key, value in info.items():
            output += f"  {key}: {value}\n"
        output += "\n"

        #Print to screen
        print(output)
        #Write to USB file
        f.write(output)    
print(f"Solar System Notes saved to {usbPath} ")    


I wrote it in way that can be saved on both my USB DRIVE and on my computer.



==========OUTPUT==========
===CORNELIUS-SNOWHYT'S SOLAR SYSTEM NOTES===


1. Mercury
  Description: Closet palnet to the sun. Small, rocky.
  Moons: 0
  Revolution: 88 Earth days
  Rotation: 59 Earth days (prograde, like the Earth ie anticlockwise)
  Diameter: 4,880 km
  Supports Life: No
  Discovery: Known since ancient times (Prehistoric observations) by Greeks, Mayans, Babylonians. Visble to the naked eye, but first studied by Mriner 10 Spacecraft in 1974-75
  Distance from the sun: 57.9 million km (0.39 AU)


2. Venus
  Description: Hottest planet, rocky with volcanic plains and thick Carbon dioxide(CO2) atmosphere.
  Moons: 0
  Revolution: 225 Earth days
  Rotation: 243 Earth days (retrograde ie clockwise so the sun rises in the West and sets in the East )
  Diameter: 12.104 km
  Supports Life: No
  Dicovery: Known since ancient times(Prehistoric observations) by Greeks, Babylonians, Mayans. Bightest object in the the sky after the Moon; detailed mapping by Magellan spacecraftin 1990s
  Distance from the sun: 108.2 million km (0.72 AU)


3. Earth
  Description: Our home planet, silcate crust, oceans and continents.
  Moons: 1
  Revolution: 365 days
  Rotation: 24 hours (prograde)
  Diameter: 12,742 km
  Supports Life: Yes
  Discovery: NA, Studied since ancient times: modern understanding from satelites and space misions 1960-70s
  Distance from the sun: 149.6 million km (1 AU)


4. Mars
  Description: Known since ancient times ; studied by Mariner 4 (1965)
  Moons: 2
  Revolution: 687 Earth days
  Rotation: 24.6 hours (prograde, like Earth)
  Diameter: 6,779 km
  Supports Life: no (but may have supported life in the past)


5. Jupiter
  Description: Largest planet, gas giant with thick atmosphere and GreatRedSpot storm.
  Moons: 95
  Revolution: 12 Earth years
  Rotation: 10 hours (fastest rotation, prograde)
  Diameter: 139,820 km
  Support Life: No (but moon like Europa may)
  Discovered: Known since ancient times; Galileo discovered its 4 large moons (Io, Europa, Ganymede, Callisto) in 1610
  Distance from the sun: 778.5 million km (5.2 AU)


6. Saturn
  Description: Gas giant famous for its Rings made of ice and rocks
  Moons: 146
  Revolution: 29 Earth years
  Rotation: 10.7 hours (prograde)
  Diameter: 116,460 km
  Supports Life: No (Titan moon may support conditions for life)
  Discovery: Known since ancient times; rings first observerd by Galileo in 1610
  Distance from the sun: 1.43 billion km (9.58 AU)


7. Uranus
  Description: an ice giant with methane atmosphere, tilted on its side (98D)
  Moons: 27
  Revolution: 84 Earth years
  Rotation: 17 hours (retrograde)
  Diameter: 50,734 km
  Supports Life: No
  Discovery: William Herschell in 1781, first planet found with a telescope
  Distance from the sun: 2.87 billion km (19.22 AU)


8. Neptune
  Description: Ice giant with supersonic winds and methane-rich atmophere.
  Moons: 14
  Revolution: 165 Earth years
  Rotation: 16 hours (prograde)
  Diameter: 49,244 km
  Supports Life: No
  Discovered: 1846 by JonhsonGaile & Heinrich d'Arrest, based on Urbain Le Verrier's calcultions
  Distance from the sun: 4.5 billion km (30.05 AU)


Solar System Notes saved to /media/snow/USB DRIVE/worldPlanetsQuiz.txt 
snow@snow-Lenovo-IdeaPad-U410-Touch:~/Documents$ 
