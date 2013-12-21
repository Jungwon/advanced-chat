# Chat app written in node.js and socket.io

## Libraries used
<ul>
  <li>node.js / npm</li>
  <li>socket.io</li>
  <li>express</li>
  <li>node-uuid</li>
  <li>underscore</li>
  <li>ejs</li>
</ul>

# Functionality
<ul>
  <li>People are able to join the chat server after entering their names</li>
  <li>Usernames are unique - if a username is taken, a new suggestion is generated</li>
  <li>User agent and geo location are both detected</li>
  <li>People can setup a room. Room names are unique. One person can create on room and join one room</li>
  <li>Users have to join a room to chat, except for the whisper feature.</li>
  <li>Whisper messages are private messages sent between two users</li>
  <li>With a WebSpeech enabled browsers, users can record their messages</li>
  <li>Users can leave a room and/or disconnect from the server anytime</li>
</ul>

## Setup and configuration

Make sure that you update <strong>server.js</strong>:
<pre>server.listen(3000, "192.168.56.102",  function(){
  console.log("Express server up and running.");
});</pre>
and add your own IP address/hostname.

Please also update <strong>public/js/client.js</strong>:
<pre>var socket = io.connect("192.168.56.102:3000");</pre>
with the right IP address/hostname.

To install <code>npm install && bower install</code> and to launch run <code>npm start</code>.

### Whisper

To send a 'private' message, use the following format in the chat message input box:
<code>w:USERNAME:MESSAGE</code> (where 'USERNAME' is the exact name of the user who you wish to whisper to (case-sensitive). For your convenience you can use the whipser link next to the person's username on the left hand side.)

New up to date post: 

Previous articles related to this topic:
<ul>
  <li>http://tamas.io/chat-2-0-supercharged-chat-written-in-node-js-and-socket-io/</li>
  <li>http://tamas.io/simple-chat-application-using-node-js-and-socket-io/</li>
  <li>http://tamas.io/advanced-chat-using-node-js-and-socket-io-episode-1/</li>
</ul>
