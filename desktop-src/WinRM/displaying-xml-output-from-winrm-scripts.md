---
title: Exibindo a saída XML de scripts do WinRM
description: Windows Os scripts de gerenciamento remoto retornam XML em vez de objetos. O XML não está em um formato legível. você pode usar os métodos da API MSXML e o arquivo XSL pré-instalado para transformar os dados em um formato legível por humanos.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680016"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Exibindo a saída XML de scripts do WinRM

Windows Os scripts de gerenciamento remoto retornam XML em vez de objetos. O XML não está em um formato legível. você pode usar os métodos da API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) e o arquivo XSL pré-instalado para transformar os dados em um formato legível por humanos.

para obter mais informações sobre a saída xml do WinRM e exemplos de xml brutos e formatados, consulte [scripting in Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md).

A ferramenta de linha de comando **WinRM** vem com um arquivo de transformação chamado WsmTxt. xsl que exibe a saída em um formato de tabela. se o script fornecer esse arquivo para os métodos de MSXML que executam transforma, a saída aparecerá da mesma forma que a saída da ferramenta **Winrm** .

**Para formatar a saída XML bruta**

1.  Crie o objeto [**WSMan**](wsman.md) e crie uma sessão.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  crie MSXML objetos que representam a saída de resposta XML e a transformação XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Obter dados por meio de métodos de objeto de [**sessão**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  forneça a resposta para o método MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) e o método [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) para armazenar o arquivo de transformação.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Use o método MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) e exiba ou salve a saída.

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

a sub-rotina a seguir usa chamadas para os métodos de script MSXML para fornecer a saída para WsmTxt. xsl.


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

[sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> </dl>

 

 