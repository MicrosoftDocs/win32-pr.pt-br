---
title: Enumerando ou listando todas as instâncias de um recurso
description: O método Session.Enumerate é a Windows gerenciamento remoto para obter todas as instâncias de um recurso especificado.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f510d0e0cc8115ca4dca7c7e46dd5e987ef0dd15dd4fa7d92e47d737e467d8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679986"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Enumerando ou listando todas as instâncias de um recurso

O [**método Session.Enumerate**](session-enumerate.md) é a Windows de Gerenciamento Remoto para obter todas as instâncias de um recurso especificado.

O método [**Session.Enumerate**](session-enumerate.md) não obtém uma coleção em um objeto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) como uma chamada [**cQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) doSWbemService.Execom uma consulta [WMI](/windows/desktop/WmiSdk/querying-wmi) como um parâmetro (por exemplo, ) ou uma chamada para um método como `ExecQuery("SELECT * from Win32_LogicalDisk")` [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). Os métodos de objeto **Session.Enumerate** e [**Enumerator**](enumerator.md) são muito mais semelhantes à operação do objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script que é usado para ler arquivos como um fluxo.

Para ler arquivos como um fluxo de texto, você deve criar o objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script e chamar o [método TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) para ler cada linha do arquivo. De maneira semelhante, você pode chamar o método [**Session.Enumerate**](session-enumerate.md) para obter um objeto [**Enumerator**](enumerator.md) e chamar o [**método Enumerator.ReadItem**](enumerator-readitem.md) para obter o próximo item. Como é o caso ao ler do arquivo de texto, você pode chamar a propriedade [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) para verificar se você atingiu o final dos itens de dados.

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

    

3.  Chame o [**método Session.Enumerate.**](session-enumerate.md) Essa chamada inicia uma enumeração. No WinRM, uma operação de enumeração não obtém uma coleção da mesma maneira que o WMI. Em vez disso, **o método Session.Enumerate** estabelece um WS-Management de enumeração de protocolo que é mantido no [**objeto Enumerator.**](enumerator.md)

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Chame o [**método Enumerator.ReadItem**](enumerator-readitem.md) para obter o próximo item dos resultados. No WS-Management, isso corresponde à operação de pull. Use o [**método Enumerator.AtEndOfStream**](enumerator-atendofstream.md) como um controle para saber quando parar de ler.

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

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Usando Windows gerenciamento remoto](using-windows-remote-management.md)
</dt> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> </dl>

 

 