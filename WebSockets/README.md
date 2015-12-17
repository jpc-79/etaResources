From Chris Arneson via Slack:

http is a request-response protocol; the client only gets data when/if it asks for it. So if the client wants to get frequent updates, it has to “poll” the server, for example once a second if it wants make sure its data is at worst one second stale. Modern browsers support a related protocol called WebSockets for real-time bi-directional client-server communication. If your project requires real-time client updates, that’s the way to go. Here’s an example of how it works:

[Live Deployment](https://eta-buzz.herokuapp.com)

[Server-Side Code](https://github.com/carnesen/buzz/blob/master/app.js#L124)

[Client Side Code](https://github.com/carnesen/buzz/blob/master/public/js/app.js#L16)

To get the full effect, open the app in two windows and notice how updates in one propagate immediately to the other. The [“socket.io”](http://socket.io) library makes WebSockets relatively easy to set up.
