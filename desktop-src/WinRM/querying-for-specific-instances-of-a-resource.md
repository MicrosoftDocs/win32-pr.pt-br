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
# <a name="querying-for-specific-instances-of-a-resource"></a><span data-ttu-id="2b51a-103">Consultando instâncias específicas de um recurso</span><span class="sxs-lookup"><span data-stu-id="2b51a-103">Querying for Specific Instances of a Resource</span></span>

<span data-ttu-id="2b51a-104">A chamada para [**Session. enumera**](session-enumerate.md) tem parâmetros opcionais que restringem a enumeração em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="2b51a-104">The call to [**Session.Enumerate**](session-enumerate.md) has optional parameters that narrow the enumeration into a query.</span></span> <span data-ttu-id="2b51a-105">Como a [API de script do WinRM](winrm-scripting-api.md) e a [API C++ do WinRM](winrm-c---api.md) estão modeladas com mais detalhes no protocolo de WS-Management subjacente, os parâmetros usam a mesma terminologia para consulta como o dialeto de *filtro* e *filtro*.</span><span class="sxs-lookup"><span data-stu-id="2b51a-105">Because the [WinRM Scripting API](winrm-scripting-api.md) and the [WinRM C++ API](winrm-c---api.md) are closely modeled on the underlying WS-Management protocol, the parameters use the same terminology for querying as the protocol—*filter* and *filter dialect*.</span></span>

<span data-ttu-id="2b51a-106">Você pode usar os parâmetros de filtro e dialeto de [**Session. enumerar**](session-enumerate.md) ou pode construir e fornecer um objeto [**ResourceLocator**](resourcelocator.md) e o método [**addseletor**](resourcelocator-addselector.md) , mas não pode fazer ambos.</span><span class="sxs-lookup"><span data-stu-id="2b51a-106">You can either use the filter and dialect parameters of [**Session.Enumerate**](session-enumerate.md) or you can construct and supply a [**ResourceLocator**](resourcelocator.md) object and the [**AddSelector**](resourcelocator-addselector.md) method, but you cannot do both.</span></span>

<span data-ttu-id="2b51a-107">Este procedimento executa uma consulta para adaptadores de rede que têm TCP/IP vinculado e habilitado.</span><span class="sxs-lookup"><span data-stu-id="2b51a-107">This procedure executes a query for network adapters that have TCP/IP bound and enabled.</span></span> <span data-ttu-id="2b51a-108">A consulta solicita todas as instâncias do [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) que têm a propriedade **IpEnabled** definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="2b51a-108">The query requests all the instances of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) that have the **IpEnabled** property set to **True**.</span></span> <span data-ttu-id="2b51a-109">Exceto pela adição do *filtro* e do *dialeto*, a consulta é tratada como uma enumeração simples.</span><span class="sxs-lookup"><span data-stu-id="2b51a-109">Except for the addition of the *filter* and *dialect*, the query is handled like a simple enumeration.</span></span>

<span data-ttu-id="2b51a-110">Neste exemplo, o nome do recurso para a constante de recurso é representado por um asterisco " \* " porque o nome da classe, [**\_ NetworkAdapterConfiguration do Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), já está mencionado na cadeia de caracteres *strFilter* .</span><span class="sxs-lookup"><span data-stu-id="2b51a-110">In this example, the resource name for the Resource constant is represented by an asterisk "\*" because the class name, [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), is already mentioned in the *strFilter* string.</span></span>

<span data-ttu-id="2b51a-111">**Para consultar instâncias específicas de um recurso**</span><span class="sxs-lookup"><span data-stu-id="2b51a-111">**To query for specific instances of a resource**</span></span>

1.  <span data-ttu-id="2b51a-112">Para facilitar a leitura, defina URIs como constantes.</span><span class="sxs-lookup"><span data-stu-id="2b51a-112">For ease-of-reading, define URIs as constants.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  <span data-ttu-id="2b51a-113">Criar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="2b51a-113">Create a session.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  <span data-ttu-id="2b51a-114">Construa a cadeia de caracteres de filtro.</span><span class="sxs-lookup"><span data-stu-id="2b51a-114">Construct the filter string.</span></span> <span data-ttu-id="2b51a-115">Gerenciamento Remoto do Windows dá suporte a [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como dialeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="2b51a-115">Windows Remote Management supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as the filter dialect.</span></span>

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  <span data-ttu-id="2b51a-116">Defina todas as [**constantes de enumeração**](enumeration-constants.md) necessárias no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="2b51a-116">Set any required [**enumeration constants**](enumeration-constants.md) in the *flags* parameter.</span></span>

    <span data-ttu-id="2b51a-117">Lembre-se de que, se os sinalizadores incluírem as [**constantes de enumeração**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** ou **WSManFlagHierarchyShallow** , o serviço WinRM retornará o erro de código de erro no **modo de polimorfismo do \_ WSMan \_ \_ \_ sem suporte**.</span><span class="sxs-lookup"><span data-stu-id="2b51a-117">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then WinRM service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

5.  <span data-ttu-id="2b51a-118">Chame o método [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="2b51a-118">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="2b51a-119">Essa chamada inicia uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="2b51a-119">This call starts an enumeration.</span></span> <span data-ttu-id="2b51a-120">O método **Session. enumera** estabelece um contexto de enumeração de protocolo WS-Management, mantido no objeto [**Enumerator**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="2b51a-120">The **Session.Enumerate** method establishes a WS-Management protocol enumeration context, maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  <span data-ttu-id="2b51a-121">Chame o método [**Enumerator. ReadItem**](enumerator-readitem.md) para obter o próximo item dos resultados.</span><span class="sxs-lookup"><span data-stu-id="2b51a-121">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="2b51a-122">No protocolo WS-Management, isso corresponde à operação de pull.</span><span class="sxs-lookup"><span data-stu-id="2b51a-122">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="2b51a-123">Use o método [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) como um controle para saber quando parar de ler.</span><span class="sxs-lookup"><span data-stu-id="2b51a-123">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

<span data-ttu-id="2b51a-124">O exemplo de código VBScript a seguir mostra o script completo.</span><span class="sxs-lookup"><span data-stu-id="2b51a-124">The following VBScript code example shows the complete script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2b51a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b51a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b51a-126">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="2b51a-126">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="2b51a-127">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="2b51a-127">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="2b51a-128">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="2b51a-128">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 