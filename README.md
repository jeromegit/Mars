# Mars
A new line of code
Yet another line of code

```nomnoml
#.action: fill=#8f8 visual=input
 
[<lollipop>start]->[<action>indicate]
[indicate]->[<sender>reject]
[reject]->[<end> e]
[indicate]->[<sender>ack]
 
[ack]->[<action>cancel]
[ack]->[<action>replace]
 
[cancel]->[<sender>cancel_reject]
[cancel_reject]->[<end>e]
[cancel]->[<sender>canceled]
[canceled]->[<end>e]
 
[replace]->[<sender>replaced]
[replace_reject]->[<end>e]
[replace]->[<sender>replace_reject]
[replaced]->[ack]
 
[ack]->[<sender>invite]
[invite]->[<action>firmup]
[invite]->[e]
 
[firmup]->[<sender>firm_reject]
[firm_reject]->[<end>e]
[firmup]->[<sender>firm_ack]
[firm_ack]->[<sender>DFD]
[DFD]->[e]
[firm_ack]->[<sender>filled]
[filled]->[e]
 
[firm_ack]->[<sender>partial]
[partial]->[DFD]
[partial]->[filled]
[partial]->[partial]
 
[firm_ack]->[<action>firm_cancel]
[firm_cancel]->[<sender>firm_cancel_reject]
[firm_cancel]->[<sender>firm_canceled]
[firm_cancel_reject]->[e]
[firm_canceled]->[e]
 
[firm_ack]->[<action>firm_replace]
[firm_replace]->[<sender>firm_replace_reject]
[firm_replace_reject]->[e]
[firm_replace]->[<sender>firm_replaced]
[firm_replaced]->[firm_ack]
```
