# CS-230-Operating-Platforms-The-Gaming-Room-Software-Design-Document[README (1).md](https://github.com/user-attachments/files/33941496/README.1.md)
# CS 230 Operating Platforms: The Gaming Room Software Design Document

This folder contains the software design document I completed for The Gaming Room in CS 230 Operating Platforms at Southern New Hampshire University.

**File:** `CS 230 Project Software Design Document.docx`

## Reflection

### Who was the client, and what did they want?

The client was The Gaming Room, a company with an Android game called Draw It or Lose It. In the game, teams guess a puzzle while a stock drawing appears on screen over four one-minute rounds. The Gaming Room wanted to turn it into a web-based game that people could play on any device. Their requirements were that a game could have one or more teams, each team could have multiple players, game and team names had to be unique, and only one instance of the game service could exist in memory at a time. Across the course, I wrote a design document that covered the domain model, an evaluation of Linux, Mac, Windows, and mobile platforms, and a final recommendation for the server platform.

### What did I do particularly well?

I think I did well at connecting each section back to the client's actual requirements. In the Domain Model, I explained how the singleton pattern in GameService keeps only one instance in memory, and how the Entity base class lets Game, Team, and Player share an ID and a name. I also kept my recommendation consistent from start to finish. My Evaluation pointed toward Linux, and the Recommendations section built on that choice instead of starting over.

### What was helpful about working through a design document?

Working through the UML diagram before writing code made the relationships between classes clear. Once I understood that GameService hands out unique IDs and checks names, I knew exactly where that logic belonged in the code. The document also made me think about problems I would not have noticed while coding, such as what happens to the singleton if the game runs on more than one server.

### What would I revise?

I would revise the Evaluation table. The cells became long and dense, so the comparison between platforms is harder to see at a glance than it should be. I would shorten each cell to the most important points, cite sources for the licensing costs, and add a short summary under the table so the client could compare the platforms quickly.

### How did I interpret the user's needs?

I looked at the requirements from the player's side as well as the client's. Players needed to join from Windows, Mac, Linux, iOS, or Android, so I recommended a responsive web interface instead of separate apps. The drawings also had to appear on time, so I recommended a server-controlled timer, WebSockets, and a CDN for the images. Considering the user's needs matters because a design can meet every technical requirement and still fail if the game is slow or does not work on the device someone owns.

### How did I approach designing software, and what would I do next time?

I started with the requirements and the UML diagram, then moved outward to the constraints, platforms, memory, storage, networking, and security. Breaking the problem into these layers helped me make decisions one at a time while keeping them connected. In the future, I would keep using UML diagrams and a requirements checklist, and I would add a simple architecture diagram earlier so the client and developers can see how all of the parts fit together. I would also compare platforms with clearer criteria, such as cost, scalability, and security, so the reasoning behind the recommendation is easy to follow.
