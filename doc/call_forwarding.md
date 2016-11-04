Call forwarding AT+CCFC format

AT+CCFC=<type>,<action>,["<number>"]

type:
    0 unconditional
    1 mobile busy
    2 noreply
    3 not reachable
    4 all call forwarding (refer GSM 02.30 [19])
    5 all conditional call forwarding (refer GSM 02.30 [19])

action:
    0 disable
    1 enable
    2 query status
    3 registration
    4 erasure

number: where to redirect call
    
Example
AT+CCFC=1,1 - enable call forwarding for mobile busy
AT+CCFC=1,3,"0xxxxxxxx" - forward call to 0xxxxxxxx

Response:

+CCFC: 0,0,"",129,,,
Call forwarding is disabled

+CCFC: 1,1,"+37379493111",145,,,
Call forwarding is enabled