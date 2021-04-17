---
title: Consultando instâncias específicas de um recurso
description: A chamada para Session. enumera tem parâmetros opcionais que restringem a enumeração em uma consulta.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105798393"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Consultando instâncias específicas de um recurso

A chamada para [**Session. enumera**](session-enumerate.md) tem parâmetros opcionais que restringem a enumeração em uma consulta. Como a [API de script do WinRM](winrm-scripting-api.md) e a [API C++ do WinRM](winrm-c---api.md) estão modeladas com mais detalhes no protocolo de WS-Management subjacente, os parâmetros usam a mesma terminologia para consulta como o dialeto de *filtro* e *filtro*.

Você pode usar os parâmetros de filtro e dialeto de [**Session. enumerar**](session-enumerate.md) ou pode construir e fornecer um objeto [**ResourceLocator**](resourcelocator.md) e o método [**addseletor**](resourcelocator-addselector.md) , mas não pode fazer ambos.

Este procedimento executa uma consulta para adaptadores de rede que têm TCP/IP vinculado e habilitado. A consulta solicita todas as instâncias do [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) que têm a propriedade **IpEnabled** definida como **true**. Exceto pela adição do *filtro* e do *dialeto*, a consulta é tratada como uma enumeração simples.

Neste exemplo, o nome do recurso para a constante de recurso é representado por um asterisco " \* " porque o nome da classe, [**\_ NetworkAdapterConfiguration do Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), já está mencionado na cadeia de caracteres *strFilter* .

**Para consultar instâncias específicas de um recurso**

1.  Para facilitar a leitura, defina URIs como constantes.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  Criar uma sessão.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  Construa a cadeia de caracteres de filtro. Gerenciamento Remoto do Windows dá suporte a [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como dialeto de filtro.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Defina todas as [**constantes de enumeração**](enumeration-constants.md) necessárias no parâmetro *flags* .

    Lembre-se de que, se os sinalizadores incluírem as [**constantes de enumeração**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , o serviço WinRM retornará o erro de código de erro no **modo de polimorfismo do \_ WSMan \_ \_ \_ sem suporte**.

5.  Chame o método [**Session. Enumerate**](session-enumerate.md) . Essa chamada inicia uma enumeração. O método **Session. enumera** estabelece um contexto de enumeração de protocolo WS-Management, mantido no objeto [**Enumerator**](enumerator.md) .

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Chame o método [**Enumerator. ReadItem**](enumerator-readitem.md) para obter o próximo item dos resultados. No protocolo WS-Management, isso corresponde à operação de pull. Use o método [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) como um controle para saber quando parar de ler.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

O exemplo de código VBScript a seguir mostra o script completo.


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 