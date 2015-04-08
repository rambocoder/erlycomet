# Introduction #

Just some notes I'm keeping on how I'll implement json comment filtering in erlycomet.  Comments welcome.


# Details #

## To Do list ##

  * look for "json-comment-filtered": true in ext field of /meta/handshake message
  * keep track of all connections that support comment filtered content
  * support sending  messages in "json-comment-filtered" format.
  * set Content-Type of outgoing comment filtered messages to 'text/json-comment-filtered'.

## Questions ##

  * Do we need to support receiving messages in "json-comment-filtered" format?