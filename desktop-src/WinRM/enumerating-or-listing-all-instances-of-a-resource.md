---
title: Enumerando ou listando todas as instâncias de um recurso
description: O método Session. Enumeration é a abordagem Gerenciamento Remoto do Windows para obter todas as instâncias de um recurso especificado.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162360"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Enumerando ou listando todas as instâncias de um recurso

O método [**Session. Enumeration**](session-enumerate.md) é a abordagem gerenciamento remoto do Windows para obter todas as instâncias de um recurso especificado.

O método [**Session. Enumerate**](session-enumerate.md) não obtém uma coleção em um objeto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) como uma chamada [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) com uma [consulta WMI](/windows/desktop/WmiSdk/querying-wmi) como um parâmetro (por exemplo, `ExecQuery("SELECT * from Win32_LogicalDisk")` ) ou uma chamada para um método como [**SWbemObject. Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). **Session. enumera** e os métodos do objeto [**Enumerator**](enumerator.md) são muito mais semelhantes à operação do objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script usado para ler arquivos como um fluxo.

Para ler arquivos como um fluxo de texto, você deve criar o objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script e chamar o método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para ler cada linha do arquivo. De forma semelhante, você pode chamar o método [**Session. enumerar**](session-enumerate.md) para obter um objeto [**Enumerator**](enumerator.md) e chamar o método [**Enumerator. ReadItem**](enumerator-readitem.md) para obter o próximo item. Como é o caso ao ler do arquivo de texto, você pode chamar a propriedade [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) para verificar se você atingiu o final dos itens de dados.

**Para enumerar um recurso**

1.  Criar uma sessão.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  Construa o URI para identificar o recurso.

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  Chame o método [**Session. Enumerate**](session-enumerate.md) . Essa chamada inicia uma enumeração. No WinRM, uma operação de enumeração não obtém uma coleção da mesma maneira que o WMI. Em vez disso, o método **Session. Enumerate** estabelece um contexto de enumeração de protocolo WS-Management que é mantido no objeto [**Enumerator**](enumerator.md) .

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Chame o método [**Enumerator. ReadItem**](enumerator-readitem.md) para obter o próximo item dos resultados. No protocolo WS-Management, isso corresponde à operação de pull. Use o método [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) como um controle para saber quando parar de ler.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

O exemplo de código VBScript a seguir mostra o script completo.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
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

 

 