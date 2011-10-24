xmpp_talker is a basis for building XMPP bots.

Description:

	It sits and waits for incoming messages. When it gets one, it creates a new
	worker process and gives the message's from-jid and its body for processing.

	When the job in the worker process is done it casts back a jid-to and a body2, 
	to xmpp_talker.	xmpp_talker sends a new message to-jid with body2. This is it.

	In case connection interruption it also tries to re-connect.

	For more info see source code of xmpp_talker.erl - it is with comments.

Requirements:
	exmpp (https://support.process-one.net/doc/display/EXMPP/exmpp+home)
	
To start:
	Edit xmpp_talker_sup.erl, insert your JID and password and you good to go!