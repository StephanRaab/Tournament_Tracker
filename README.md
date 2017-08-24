# Tournament Tracker

## Requirements
1. Tracks games played and their outcome(who won)
2. Multiple competitors play in the tournament
3. Creates a tournament plan (who plays in what order)
4. Schedules games
5. A single loss eliminates a player
6. The last player standing is the winner

### Secondary questions
1. How many players will the tournament handle? Is it a variable?
    *The application should be able to handle a variable number of players in a tournament.*
2. If a tournament has less than the full complement of players, how do we handle it?
    *A tournament with less than the perfect number (2, 4, 8, ...) should add in "byes". Basically, certain people selected at random get to skip the first round and act as if they won.*
3. Should the ordering of who plays each other be random or ordered by input order?
    *The ordering of the tournament should be random.*
4. Should we schedule a game or are they just played whenever?
    *The games should be played in whatever order and whenever the players want to play them.*
5. If the games are scheduled, how does the system know when to schedule games for?
    *see answer 4.*
6. If the games are played whenever, can a game from the second round be played before the first round is complete?
    *No. Each round should be fully completed before the next round is displayed.*
7. Does the system need to store a score of some kind or just who won?
    *Storing a simple score would do the trick. So either a 0 or a 1.*
8. What type of front-end should the system have?
    *The system should be a desktop system for now, down the road it would be nice to turn it into an app or a website.*
9. Where will the data be stored?
    *Ideally, the data would be stored in MS SQL db but please keep option to store to a text file instead.*
10. Will this system handle entry fees, prizes, or other payouts?
    *Yes. It should have an option to charge an entree fee. The total cash amount should not exceed the income from the tournament. A percentage based system would also be nice to specify.*
11. What type of reporting is needed?
    *A simple report specifying the outcome of the games per round  as well as a report that specifies who won and how much they won. These can be displayed on a form or they can be emailed to tournament competitors and the admin.*
12. Who can fill in the results of the game?
    *Anyone using the application should be able to fill in the game scores.*
13. Are there varying levels of access?
    *No. The only method of varied access is if the competitors are not allowed into the application and instead, they do everything by email.*
14. Should this system contact users about upcoming games?
    *Yes. The system should email users that they are due to play in a round as well as who they are scheduled to play.*
15. Is each player on their own or can teams use this tournament tracker?
    *The tournament tracker should be able to handle the addition of other members. Teams should also be able to name their team.*

# Big Picture Design
**Structure:** Windows Forms application and Class Library
**Data:** SQL and/or Text File
**Users:** One at a time on one application

## Key Concepts
    - Email
    - SQL
    - Custom Events
    - Error Handling
    - Interfaces
    - Random Ordering
    - Texting
