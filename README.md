# SPPD
SPPDProtocol

FB case<br>
Heade:Byte;&nbsp;->&nbsp;Length:Tid&nbsp;->&nbsp;Mode:Word;<br>
FB&nbsp;&nbsp;&nbsp;&nbsp;FF&nbsp;FF&nbsp;FF&nbsp;FF&nbsp;&nbsp;&nbsp;&nbsp;FF&nbsp;FF




PacketHeader Struct

Header Cases:<br>
Byte&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;$F0;<br>
Byte&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;$FB;

THeader = packed<br>
&nbsp;&nbsp;&nbsp;&nbsp; Header  = Byte; <br>
&nbsp;&nbsp;&nbsp;&nbsp; aSize   = Tid; <br>
end;


Send Deck Reply
<table style="width: 534px;">
<tbody>
<tr>
<td style="width: 10px; text-align: center;">head</td>
<td style="width: 187px; text-align: center;">Size</td>
<td style="width: 201px; text-align: center;">op</td>
<td style="width: 68px; text-align: center;">sOp</td>
<td style="width: 115px; text-align: center;">sOp count</td>
<td style="width: 10px; text-align: center;">&nbsp;Unk</td>
<td style="width: 65px; text-align: center;">&nbsp;End</td>
</tr>
<tr>
<td style="width: 10px; text-align: center;">FB</td>
<td style="width: 187px; text-align: center;">00 00 00 0F</td>
<td style="width: 201px; text-align: center;">00 01 F3 03</td>
<td style="width: 68px; text-align: center;">FC</td>
<td style="width: 115px; text-align: center;">00 00</td>
<td style="width: 10px; text-align: center;">&nbsp;2A</td>
<td style="width: 65px; text-align: center;">00 00&nbsp;</td>
</tr>
</tbody>
</table>

