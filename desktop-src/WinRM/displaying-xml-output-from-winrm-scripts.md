---
title: Exibindo a saída XML de scripts do WinRM
description: Os scripts de Gerenciamento Remoto do Windows retornam XML em vez de objetos. O XML não está em um formato legível. Você pode usar os métodos da API do MSXML e o arquivo XSL pré-instalado para transformar os dados no formato legível por humanos.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007941"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Exibindo a saída XML de scripts do WinRM

Os scripts de Gerenciamento Remoto do Windows retornam XML em vez de objetos. O XML não está em um formato legível. Você pode usar os métodos da API do [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) e o arquivo XSL pré-instalado para transformar os dados no formato legível por humanos.

Para obter mais informações sobre a saída XML do WinRM e exemplos de XML brutos e formatados, consulte [scripting in Gerenciamento remoto do Windows](scripting-in-windows-remote-management.md).

A ferramenta de linha de comando **WinRM** vem com um arquivo de transformação chamado WsmTxt. xsl que exibe a saída em um formato de tabela. Se o script fornecer esse arquivo para os métodos do MSXML que executam o transforma, a saída aparecerá da mesma forma que a saída da ferramenta **WinRM** .

**Para formatar a saída XML bruta**

1.  Crie o objeto [**WSMan**](wsman.md) e crie uma sessão.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Crie objetos MSXML que representam a saída de resposta XML e a transformação XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Obter dados por meio de métodos de objeto de [**sessão**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Forneça a resposta para o método [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) do MSXML e o método [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) para armazenar o arquivo de transformação.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Use o método [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) do MSXML e exiba ou salve a saída.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

O exemplo de código VBScript a seguir mostra o script completo.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Adicionando uma sub-rotina portátil para transformar XML em seus scripts

Você pode adicionar uma sub-rotina a seus scripts que usa o arquivo XSL pré-instalado para converter a saída XML bruta de um script do WinRM em um formulário tabular.

A sub-rotina a seguir usa chamadas para os métodos de script MSXML para fornecer a saída para WsmTxt. Xsl.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



A seguinte sub-rotina transforma cada linha de seus dados, conforme mostrado no exemplo a seguir.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Referência de Gerenciamento Remoto do Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 