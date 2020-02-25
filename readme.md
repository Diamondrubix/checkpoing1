Session based dynamically spun up server.
This is a framework to spin up a short lived server to serve a small group of users for a short amount of time. The “matchmaker” server will connect the users (for now 2 users) together, and spin up a new server in a container for them to then communicate (imagine a video game server or chat room etc) They user the server for the time they need (no longer than 24 hour in general) and then the results of the server are saved and the server dies, sending any still connected users back to the matchmaking server.


Test cases
Can send message from person 1 to person 2
Person 3 cannot see or send messages to person 1 or 2 (should not be able to connect)
Person 3 and 4 can communicate 100% independent of person 1 and 2
If person 1 leaves, person 2 gets notified and then disconnected
If person 1 joins the server, but person 2 never connects, person 1 is eventually notified and disconnected.
If there is nobody on the server, the server should die.
Matchmaker should have basic login and account detail security features (password is safe, can’t see other users info etc)

Things we don’t want an attacker to do
See messages between two people.
See other peoples account info. 
Keep a server alive indefinitely.

Checkpoint 2 deliverables:



A server that we can spin up in the container (could simply be a chat room for our purposes, maybe a server for the game rock paper scissors)
Results of the game are then saved in mongodb

Checkpoint 4 deliverables:
Any nice details for the game or service we choose to host.
Kubernests automatically spinning up instances properly.

