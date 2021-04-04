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
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a><span data-ttu-id="ba873-103">Enumerando ou listando todas as instâncias de um recurso</span><span class="sxs-lookup"><span data-stu-id="ba873-103">Enumerating or Listing All Instances of a Resource</span></span>

<span data-ttu-id="ba873-104">O método [**Session. Enumeration**](session-enumerate.md) é a abordagem gerenciamento remoto do Windows para obter todas as instâncias de um recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="ba873-104">The [**Session.Enumerate**](session-enumerate.md) method is the Windows Remote Management approach to obtaining all the instances of a specified resource.</span></span>

<span data-ttu-id="ba873-105">O método [**Session. Enumerate**](session-enumerate.md) não obtém uma coleção em um objeto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) como uma chamada [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) com uma [consulta WMI](/windows/desktop/WmiSdk/querying-wmi) como um parâmetro (por exemplo, `ExecQuery("SELECT * from Win32_LogicalDisk")` ) ou uma chamada para um método como [**SWbemObject. Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="ba873-105">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in a [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) object like a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) call with a [WMI query](/windows/desktop/WmiSdk/querying-wmi) as a parameter (for example, `ExecQuery("SELECT * from Win32_LogicalDisk")`), or a call to a method like [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span> <span data-ttu-id="ba873-106">**Session. enumera** e os métodos do objeto [**Enumerator**](enumerator.md) são muito mais semelhantes à operação do objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script usado para ler arquivos como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="ba873-106">**Session.Enumerate** and the [**Enumerator**](enumerator.md) object methods are much more similar to the operation of the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object that is used for reading files as a stream.</span></span>

<span data-ttu-id="ba873-107">Para ler arquivos como um fluxo de texto, você deve criar o objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script e chamar o método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para ler cada linha do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ba873-107">To read files as a text stream, you must create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="ba873-108">De forma semelhante, você pode chamar o método [**Session. enumerar**](session-enumerate.md) para obter um objeto [**Enumerator**](enumerator.md) e chamar o método [**Enumerator. ReadItem**](enumerator-readitem.md) para obter o próximo item.</span><span class="sxs-lookup"><span data-stu-id="ba873-108">In a similar way, you can call the [**Session.Enumerate**](session-enumerate.md) method to obtain an [**Enumerator**](enumerator.md) object and call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to get the next item.</span></span> <span data-ttu-id="ba873-109">Como é o caso ao ler do arquivo de texto, você pode chamar a propriedade [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) para verificar se você atingiu o final dos itens de dados.</span><span class="sxs-lookup"><span data-stu-id="ba873-109">As is the case when reading from the text file, you can call the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

<span data-ttu-id="ba873-110">**Para enumerar um recurso**</span><span class="sxs-lookup"><span data-stu-id="ba873-110">**To enumerate a resource**</span></span>

1.  <span data-ttu-id="ba873-111">Criar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="ba873-111">Create a session.</span></span>

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  <span data-ttu-id="ba873-112">Construa o URI para identificar o recurso.</span><span class="sxs-lookup"><span data-stu-id="ba873-112">Construct the URI to identify the resource.</span></span>

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  <span data-ttu-id="ba873-113">Chame o método [**Session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="ba873-113">Call the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="ba873-114">Essa chamada inicia uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="ba873-114">This call starts an enumeration.</span></span> <span data-ttu-id="ba873-115">No WinRM, uma operação de enumeração não obtém uma coleção da mesma maneira que o WMI.</span><span class="sxs-lookup"><span data-stu-id="ba873-115">In WinRM, an enumeration operation does not obtain a collection in the same way that WMI does.</span></span> <span data-ttu-id="ba873-116">Em vez disso, o método **Session. Enumerate** estabelece um contexto de enumeração de protocolo WS-Management que é mantido no objeto [**Enumerator**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="ba873-116">Instead, the **Session.Enumerate** method establishes a WS-Management protocol enumeration context that is maintained in the [**Enumerator**](enumerator.md) object.</span></span>

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  <span data-ttu-id="ba873-117">Chame o método [**Enumerator. ReadItem**](enumerator-readitem.md) para obter o próximo item dos resultados.</span><span class="sxs-lookup"><span data-stu-id="ba873-117">Call the [**Enumerator.ReadItem**](enumerator-readitem.md) method to obtain the next item of the results.</span></span> <span data-ttu-id="ba873-118">No protocolo WS-Management, isso corresponde à operação de pull.</span><span class="sxs-lookup"><span data-stu-id="ba873-118">In WS-Management protocol, this corresponds to the pull operation.</span></span> <span data-ttu-id="ba873-119">Use o método [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) como um controle para saber quando parar de ler.</span><span class="sxs-lookup"><span data-stu-id="ba873-119">Use the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) method as a control to know when to stop reading.</span></span>

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

<span data-ttu-id="ba873-120">O exemplo de código VBScript a seguir mostra o script completo.</span><span class="sxs-lookup"><span data-stu-id="ba873-120">The following VBScript code example shows the complete script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ba873-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba873-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba873-122">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="ba873-122">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ba873-123">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="ba873-123">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ba873-124">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="ba873-124">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 