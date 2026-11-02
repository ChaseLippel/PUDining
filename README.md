# PUDining

A Java command-line tool that checks every Purdue dining court's menu for your favorite foods and tells you where to eat today.

## The Problem

Purdue has a lot of dining courts with menus that change every meal, so finding out when my favorite foods are being served means checking each dining court one by one. I often skip going to the dining hall when my favorite food is being served because I am too lazy to check.

## How It Works 

- Fetch the entire dining court menu and all the foods being served that day
- Grab a list filled with favorite foods of the USER
- Parse the two lists
- Compare the two lists and return the best possible dining court for that day

![System Diagram](System%20Diagram.png)

The full feature breakdown is in the [Eisenhower Matrix](Eisenhower%20Matrix.pdf).

## Tech Stack

- **Language:** Java
- **HTTP requests:** `java.net.http.HttpClient`
- **Parsing:** Gson
- **Dates:** `java.time.LocalDate`
- **Reading files:** `java.nio.file.Files` and `Scanner`
- **Data storage:** `favorites.txt` (plain text, one favorite food per line)
- **Data source:** [Purdue Dining API](https://api.hfs.purdue.edu/menus/v2/locations/) — free and public, no API key needed
- **Version control:** Git and GitHub
- **IDE:** IntelliJ IDEA

## Project Structure

```
PUDining/
├── src/                    Java source code
├── Eisenhower Matrix.pdf   Feature planning (MVP vs. later vs. cut)
├── System Diagram.png      Flowchart of how the program works
├── System Diagram.drawio   Editable source for the diagram
└── README.md
```

## Setup

*Coming soon — setup and run instructions will be added once the MVP is built.*

## Roadmap

Planned features after the MVP (from the "Schedule" quadrant):

- [ ] Show which meal each favorite is served at and where
- [ ] Check the whole week, not just today, to make a plan
- [ ] Add or remove favorites easily with commands
- [ ] Filter by dietary options like vegan or vegetarian
- [ ] Cache each day's menu so it isn't calling the API every time
- [ ] Write JUnit tests for the logic

## Author

Chase Lippel — [@ChaseLippel](https://github.com/ChaseLippel)
