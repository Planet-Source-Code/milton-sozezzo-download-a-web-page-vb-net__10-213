<div align="center">

## Download a web page \- VB\.NET


</div>

### Description

Function to download a URL.
 
### More Info
 
New version to "Download a web page to a string" (http://www.planet-source-code.com/vb/scripts/showcode.asp?lngWId=10&txtCodeId=86)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Milton Sozezzo](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/milton-sozezzo.md)
**Level**          |Beginner
**User Rating**    |4.9 (69 globes from 14 users)
**Compatibility**  |VB\.NET
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__10-9.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/milton-sozezzo-download-a-web-page-vb-net__10-213/archive/master.zip)





### Source Code

```
Public Function GetPageHTTP(ByVal URL As String) As String
  'Ex.: dim s As string = GetPageHTTP("http://www.uol.com.br")
  'Ex.: dim x As string = GetPageHTTP("http://www.microsoft.com/")
  'Ex.: dim x As string = GetPageHTTP("http://www.planet-source-code.com/vb/default.asp?lngWId=10")
  Dim wc As New System.Net.WebClient()
  Dim s As System.IO.Stream = wc.OpenRead(URL)
  Dim r As String
  Dim sr As System.IO.StreamReader = New System.IO.StreamReader(s, System.Text.Encoding.UTF7, False)
  r = sr.ReadToEnd()
  Return r
 End Function
```

