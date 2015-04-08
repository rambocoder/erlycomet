ErlyComet allows to plug in Bayeux compliant Comet functionality in Erlang Web servers. ErlyComet ships with a sample server implementation for running the demos.

## Features: ##
  * Web server support:
    * [MochiWeb HTTP toolkit](http://mochiweb.com)
  * Javascript libraries:
    * [dojo](http://dojotoolkit.org)
    * http://jquery.com with [jquery Comet plugin](http://plugins.jquery.com/project/Comet) (from [SVN](http://code.google.com/p/jquerycomet/))
  * Transport types:
    * long-polling
    * callback-polling
  * optional Bayeux features:
    * JSON comment filtered format (to prevent Ajax Hijacking)
    * Channel globbing
    * Service channels
  * Easy pluggable custom applications (decoupled from Comet logic)
  * Designed as distributed system from ground up
  * Connection and channel management with distributed in-memory database

## Demos: ##
  * Simple echo
  * Server side counter
  * RPC (with custom serverside application)
  * Simple chat
  * Collaborative drawing

## ToDo: ##
  * create a dojo custom build for the demos
  * handle Multi frame operations (Bayeux spec section 8) to overcome the two connection limit
  * make ErlyComet run also on Crary web server
  * add authentication, load balancing
  * replace homegrown cluster management with [fragmentron](http://code.google.com/p/fragmentron/)
  * add more transport types: Flash (RTMP), iframe, ActiveX (as in gmail for IE), etc.
  * integrate with http://erlware.org
  * load testing

## Project status: ##
For using this software in production you should wait until the ToDo items have shifted up to the Features list !