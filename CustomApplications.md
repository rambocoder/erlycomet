#### 1) Calling ErlyComet handler (from MochiWeb) ####
E.g. with `erlycomet_demo_rpc` as the module name of your custom application
```
ErlyCometRequest = erlycomet_request:new(erlycomet_demo_rpc),
ErlyCometRequest:handle(Req);
```

#### 2) What you need to do at the Javascript client app ####
just pass a JSON-RPC compliant object, e.g. (from RPC demo):
```
dojox.cometd.publish("/rpc/test", { id:rpc._id, method:"delayed_echo", params:[text, delay]});
```

#### 3) Erlang custom app ####
  * Module name: as explained at 1)
  * Function name: as specified in your JSON-RPC object
  * Arguments: first Arg contains channel name, following args are as defined in JSON-RPC object
Example Function (from demo):
```
delayed_echo(<<"/rpc/test">>, Text, Delay) ->
    Timeout = list_to_integer(binary_to_list(Delay)) * 1000,
    receive
    after Timeout ->
    	Text
    end.
```