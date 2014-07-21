---
layout: post
title:  "Twitter API"
date:   2014-07-17 23:10:55
---

Just spent the last couple of hours trying to get this damn Twitter API to authenticate! I had to download a 'library' of some sort <a href="https://github.com/coldfumonkeh/monkehTweets"> (You can find it here)</a><br>
Some issues I ran into:<br>
<ul>
	<li>Session timeout was too short. The session would time out killing the variables. Trying to access the variables threw an error since they were killed when the session died</li>
	<li>I didn't set a callback in my Twitter application so my application was locked in something called 'oob' mode. Not sure what the hell that means. When I put the callback URL in the application settings, the error went away and worked as designed.</li>
</ul>

Things to remember:<br>
<ul>
	<li>If you are using an Application.cfc file, carefully merge the one included in the library with yours</li>
	<li>Make sure the sessiontimeout is long enough to actually hold the variables</li>
	<li>Read the instructions, pretty straightforward but may need to read more than once</li>
	<li>Make sure Tweet isn't duplicate or it won't post</li>
	<li>Use the index.cfm, authenticate.cfm, post.cfm example pages to get an idea of what the hell is going on</li>
	<li>cfdump is your friend!</li>
</ul>
