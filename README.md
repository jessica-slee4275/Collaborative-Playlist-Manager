<h1>Collaborative Playlist Manager with Voting</h1>
<h2>Overview</h2>
With the holiday season approaching, I wanted to create a fun and engaging game for parties with my friends. The idea is to dance to music and vote for the best songs while dancing. While Spotify already offers a Collaborative Playlist feature, it lacks a voting system. This project fills that gap by introducing a real-time voting system integrated into collaborative playlists.
<h2>Key Features</h2>
<h3>Real-time Collaborative Playlist</h3>
<ol> 
  <li>Create playlists based on specific themes or occasions.</li>
  <li>Invite friends via a unique link or code to collaborate on the playlist</li>
  <li>Seamlessly add or remove tracks.</li>
</ol>
<ol>
  <li></li>
  <li></li>
  <li></li>
</ol>
<ol>
  <li></li>
  <li></li>
  <li></li>
</ol>
<ol>
  <li></li>
  <li></li>
  <li></li>
</ol>
1.	:
o	
o	Invite friends via a unique link or code to collaborate on the playlist.
o	
2.	Song Voting and Ranking:
o	Users can upvote or downvote songs in the playlist.
o	Popular songs are dynamically sorted to appear at the top of the playlist.
3.	Real-time Data Processing:
o	All updates (song additions, deletions, or votes) are synchronized across all connected users instantly.
4.	User Management and Access Control:
o	Only playlist owners can delete songs or change the playback order.
o	Invited users can participate in collaborative actions.
5.	Enhanced User Experience:
o	Easily view the most popular songs in the playlist.
o	Receive real-time notifications for playlist updates (e.g., "User X added a new song!").
________________________________________
Core Functionalities
1. Real-time Collaborative Playlist Creation
•	Functionality:
o	Users can create a playlist tailored to a specific event or mood.
o	Friends are invited via a link or code to collaborate.
•	Key API:
o	/v1/playlists: Create and update playlists via Spotify API.
o	/v1/users/me: Verify playlist ownership and authenticate users.
•	Example Scenario:
o	User A creates a playlist and invites User B and C to add or remove songs.
2. Song Voting and Automatic Sorting
•	Functionality:
o	Users can vote on songs (upvote/downvote).
o	The playlist dynamically sorts songs based on their vote counts.
•	Key Technology:
o	WebSocket: Real-time updates ensure votes are immediately reflected.
o	Sorting Algorithm: Dynamically reorders songs based on vote scores.
•	Example Scenario:
o	User A adds a song, and it receives 5 upvotes, automatically moving it to the top of the playlist.
3. Real-time Data Processing
•	Functionality:
o	All changes (song additions, deletions, votes) are synchronized in real-time.
•	Key Technology:
o	WebSocket: Ensures bi-directional communication between server and clients.
o	Real-time updates for all users whenever changes occur.
•	Example Scenario:
o	User B adds a song, and User A and C instantly see the update in their playlist UI.
________________________________________
System Architecture
•	Backend:
o	Node.js (Express.js) or Python (FastAPI).
o	WebSocket (Socket.IO for real-time communication).
•	Frontend:
o	React.js or Vue.js for dynamic UI updates.
•	Database:
o	Redis: Store and cache vote data in real-time.
o	PostgreSQL: Persist playlist and user data.
