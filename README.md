<h1>Collaborative Playlist Manager with Voting</h1>
<h2>Overview</h2>
With the holiday season approaching, I wanted to create a fun and engaging game for parties with my friends. The idea is to dance to music and vote for the best songs while dancing. While Spotify already offers a Collaborative Playlist feature, it lacks a voting system. This project fills that gap by introducing a real-time voting system integrated into collaborative playlists.
<h2>Key Features</h2>
<h3>Real-time Collaborative Playlist</h3>
<ul> 
  <li>Create playlists based on specific themes or occasions.</li>
  <li>Invite friends via a unique link or code to collaborate on the playlist</li>
  <li>Seamlessly add or remove tracks.</li>
</ul>
<h3>Song Voting and Ranking</h3>
<ul>
  <li>Users can upvote or downvote songs in the playlist.</li>
  <li>Popular songs are dynamically sorted to appear at the top of the playlist.</li>
</ul>
<h3>Real-time Data Processing</h3>
<ul>
  <li>All updates (song additions, deletions, or votes) are synchronized across all connected users instantly.</li>
</ul>
<h3>User Management and Access Control</h3>
<ul>
  <li>Only playlist owners can delete songs or change the playback order.</li>
  <li>Invited users can participate in collaborative actions.</li>
</ul>
<h3>Enhanced User Experience</h3>
<ul>
  <li>Easily view the most popular songs in the playlist.</li>
  <li>Receive real-time notifications for playlist updates (e.g., "User X added a new song!").</li>
</ul>
<h2>Core Functionalities</h2>
<h3>Real-time Collaborative Playlist Creation</h3>
<ul>
  <li>Functionality</li>
  <ul>
    <li>Users can create a playlist tailored to a specific event or mood.</li>
    <li>Friends are invited via a link or code to collaborate.</li>
  </ul>
  <li>Key API</li>
  <ul>
    <li>/v1/playlists: Create and update playlists via Spotify API.</li>
    <li>/v1/users/me: Verify playlist ownership and authenticate users.</li>
  <li>Example Scenario</li>
    <ul><li>User A creates a playlist and invites User B and C to add or remove songs.</li></ul>
</ul>

<h3>Song Voting and Automatic Sorting</h3>
<ul>
  <li>Functionality</li>
  <ul>
    <li>Users can vote on songs (upvote/downvote).</li>
    <li>The playlist dynamically sorts songs based on their vote counts.</li>
  <li>Key Technology</li>
    <ul>
      <li>WebSocket: Real-time updates ensure votes are immediately reflected.</li>
      <li>Sorting Algorithm: Dynamically reorders songs based on vote scores.</li>
    </ul>
  <li>Example Scenario</li>
    <ul><li>User A adds a song, and it receives 5 upvotes, automatically moving it to the top of the playlist.</li></ul>
</ul>

<h3>Real-time Data Processing</h3>
<ul>
  <li>Functionality</li>
  <ul>
    <li>All changes (song additions, deletions, votes) are synchronized in real-time.</li>
  <li>Key Technology</li>
    <ul>
      <li>WebSocket: Ensures bi-directional communication between server and clients.</li>
      <li>Real-time updates for all users whenever changes occur.</li>
    </ul>
  <li>Example Scenario</li>
    <ul><li>User B adds a song, and User A and C instantly see the update in their playlist UI.</li></ul>
</ul>

<h2>System Architecture</h2>
<ul>
  <li>Backend</li>
  <ul>
    <li>Node.js (Express.js) or Python (FastAPI).</li>
    <li>WebSocket (Socket.IO for real-time communication).</li>
  </ul>
  <li>Frontend</li>
    <ul><li>React.js or Vue.js for dynamic UI updates.</li></ul>
  <li>Database</li>
    <ul>
      <li>Redis: Store and cache vote data in real-time.</li>
      <li>PostgreSQL: Persist playlist and user data.</li>
    </ul>
</ul>
