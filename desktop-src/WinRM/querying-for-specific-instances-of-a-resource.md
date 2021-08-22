---
title: Consultando instâncias específicas de um recurso
description: A chamada para Session.Enumerate tem parâmetros opcionais que restringem a enumeração em uma consulta.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f757b6392ec26f809004d599f6c5603629d23e8eb7a7f4b08a4f3a4ef18791a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642846"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Consultando instâncias específicas de um recurso

A chamada para [**Session.Enumerate**](session-enumerate.md) tem parâmetros opcionais que restringem a enumeração em uma consulta. Como a API de [Script WinRM](winrm-scripting-api.md) e a API do [WinRM C++](winrm-c---api.md) são modeladas de perto no protocolo WS-Management subjacente, os parâmetros usam a mesma terminologia para consultar o protocolo – filtro e dialeto de *filtro.*

Você pode usar os parâmetros de filtro e dialeto [**de Session.Enumerate**](session-enumerate.md) ou pode construir e fornecer um objeto [**ResourceLocator**](resourcelocator.md) e o [**método AddSelector,**](resourcelocator-addselector.md) mas não pode fazer ambos.

Este procedimento executa uma consulta para adaptadores de rede que têm TCP/IP vinculado e habilitado. A consulta solicita todas as instâncias do [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) que têm a propriedade **IpEnabled** definida como **True.** Exceto pela adição do filtro *e* *do dialeto*, a consulta é tratada como uma enumeração simples.

Neste exemplo, o nome do recurso para a constante Recurso é representado por um asterisco " " porque o nome da \* classe, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), já é mencionado na cadeia de caracteres *strFilter.*

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

    

3.  Construa a cadeia de caracteres de filtro. Windows O Gerenciamento Remoto dá [suporte ao WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como o dialeto do filtro.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  De acordo com as [**constantes de enumeração necessárias**](enumeration-constants.md) no parâmetro *flags.*

    Esteja ciente de que se os sinalizadores incluírem as [**Constantes**](enumeration-constants.md) de Enumeração **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow,** o serviço WinRM retornará o código de erro **ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED**.

5.  Chame o [**método Session.Enumerate.**](session-enumerate.md) Essa chamada inicia uma enumeração. O **método Session.Enumerate** estabelece um WS-Management de enumeração de protocolo, mantido no [**objeto Enumerador.**](enumerator.md)

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Chame o [**método Enumerator.ReadItem**](enumerator-readitem.md) para obter o próximo item dos resultados. No WS-Management, isso corresponde à operação de pull. Use o [**método Enumerator.AtEndOfStream**](enumerator-atendofstream.md) como um controle para saber quando parar de ler.

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

[Usando Windows gerenciamento remoto](using-windows-remote-management.md)
</dt> <dt>

[Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 