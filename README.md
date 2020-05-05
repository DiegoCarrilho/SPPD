# SPPD
SPPDProtocol

PacketHeader Struct

Headers Type:<br>
Byte&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;$F0;<br>
Byte&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;$FB;

THeader = packed<br>
&nbsp;&nbsp;&nbsp;&nbsp; Header  = Byte; <br>
&nbsp;&nbsp;&nbsp;&nbsp; aSize   = Tid; <br>
end;


