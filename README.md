<div align="center">

## mixes ASP and Javasript


</div>

### Description

A small script mixes ASP and Javasript to make messages alert or for the debugage.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Serge Munoz](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/serge-munoz.md)
**Level**          |Beginner
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |ASP \(Active Server Pages\)
**Category**       |[Debugging and Error Handling](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/debugging-and-error-handling__4-6.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/serge-munoz-mixes-asp-and-javasript__4-7564/archive/master.zip)





### Source Code

<p><font face="Verdana" size="2">&lt;%' To be able to continue the code<br>
 Sub Debug(Msg)<br>
 Msg = Replace(Msg,&quot;'&quot;,&quot;\'&quot;)<br>
 Response.Write &quot;&lt;SCRIPT LANGUAGE='JavaScript'&gt;&quot;<br>
 Response.Write &quot;if(!confirm('&quot;&amp;Msg&amp;&quot;'))&quot;<br>
 Response.Write &quot;{&quot;<br>
 Response.Write &quot;location.href = 'Stop.asp';&quot;<br>
 Response.Write &quot;}&quot;<br>
 Response.Write &quot;&lt;/SCRIPT&gt;&quot;<br>
 End Sub <br>
 %&gt; <br>
 <br>
 <br>
 <br>
 </font></p>
<p><font face="Verdana" size="2">&lt;%'To stop the code<br>
 Sub Debug(Msg)<br>
 Msg = Replace(Msg,&quot;'&quot;,&quot;\'&quot;)<br>
 Response.Write &quot;&lt;script language='JavaScript'&gt;&quot;<br>
 Response.Write &quot;alert('&quot;&amp;Msg&amp;&quot;');&quot;<br>
 Response.Write &quot;history.back();&quot;<br>
 Response.Write &quot;&lt;/script&gt;&quot;<br>
 Response.End<br>
 End Sub<br>
 %&gt;<br>
 <br>
 &lt;%If Request(&quot;Mail&quot;) = &quot;&quot; Then Msg = &quot;Mail no valide&quot;
 : Debug Msg%&gt; </font></p>

