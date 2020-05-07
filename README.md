# SPPD
SPPDProtocol

<table class="tg">
<thead>
  <tr>
    <th class="tg-omgv">0</th>
    <th class="tg-omgv">1</th>
    <th class="tg-ay88">2</th>
    <th class="tg-ay88">3</th>
    <th class="tg-ay88">4</th>
    <th class="tg-ay88">5</th>
    <th class="tg-ay88">6</th>
    <th class="tg-ay88">7</th>
    <th class="tg-ay88">8</th>
    <th class="tg-ay88"> </th>
    <th class="tg-zj9c"> </th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">-&gt;</td>
    <td class="tg-zj9c">Load Balance</td>
  </tr>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">&lt;-</td>
    <td class="tg-zj9c">Load Balance</td>
  </tr>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">02</td>
    <td class="tg-ay88">-&gt;</td>
    <td class="tg-zj9c">Battle</td>
  </tr>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">03</td>
    <td class="tg-ay88">&lt;-</td>
    <td class="tg-zj9c">Token, Match and FC&nbsp;&nbsp;&nbsp;Confirm</td>
  </tr>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">04</td>
    <td class="tg-ay88">&lt;-</td>
    <td class="tg-zj9c">Battle</td>
  </tr>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">06</td>
    <td class="tg-ay88">-&gt;</td>
    <td class="tg-zj9c">Unk 06</td>
  </tr>
  <tr>
    <td class="tg-ay88">FB</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">00</td>
    <td class="tg-ay88">01</td>
    <td class="tg-ay88">F3</td>
    <td class="tg-ay88">07</td>
    <td class="tg-ay88">&lt;-</td>
    <td class="tg-zj9c">Unk 07 </td>
  </tr>
</tbody>
</table>

PacketHeader Struct

Header Cases:<br>
Byte&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;$F0;<br>
Byte&nbsp;&nbsp;&nbsp;&nbsp;->&nbsp;&nbsp;&nbsp;&nbsp;$FB;

THeader = packed<br>
&nbsp;&nbsp;&nbsp;&nbsp; Header  = Byte; <br>
&nbsp;&nbsp;&nbsp;&nbsp; aSize   = Tid; <br>
end;

Header	FB	
FB	FFFFFFFF	FFFF

+------------------+<br>
| 0xF3 Byte[7]-[8] |<br>
+------+-----------+<br>
| 0x00 | To Server |<br>
+------+-----------+<br>
| 0x01 | To Client |<br>
+------+-----------+<br>
| 0x02 | To Server |<br>
+------+-----------+<br>
| 0x03 | To Client |<br>
+------+-----------+<br>
| 0x04 | To Client |<br>
+------+-----------+<br>
| 0x06 | To Server |<br>
+------+-----------+<br>
| 0x07 | To Client |<br>
+------+-----------+<br>

<table class="tg">
<thead>
  <tr>
    <th class="tg-0pky" colspan="2">0xF3 Byte[7]</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-za14">0x00</td>
    <td class="tg-za14">To Server</td>
  </tr>
  <tr>
    <td class="tg-za14">0x01</td>
    <td class="tg-za14">To Client</td>
  </tr>
  <tr>
    <td class="tg-za14">0x02</td>
    <td class="tg-za14">To Server</td>
  </tr>
  <tr>
    <td class="tg-za14">0x03</td>
    <td class="tg-za14">To Client</td>
  </tr>
  <tr>
    <td class="tg-za14">0x04</td>
    <td class="tg-za14">To Client</td>
  </tr>
  <tr>
    <td class="tg-za14">0x06</td>
    <td class="tg-za14">To Server</td>
  </tr>
  <tr>
    <td class="tg-za14">0x07</td>
    <td class="tg-za14">To Client</td>
  </tr>
  <tr>
    <td class="tg-za14">0x82</td>
    <td class="tg-za14">To Server</td>
  </tr>
  <tr>
    <td class="tg-za14">0x83</td>
    <td class="tg-za14">To Client</td>
  </tr>
</tbody>
</table>



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

