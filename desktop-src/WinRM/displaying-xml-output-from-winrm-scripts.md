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
# <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="aa459-105">Exibindo a saída XML de scripts do WinRM</span><span class="sxs-lookup"><span data-stu-id="aa459-105">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="aa459-106">Os scripts de Gerenciamento Remoto do Windows retornam XML em vez de objetos.</span><span class="sxs-lookup"><span data-stu-id="aa459-106">Windows Remote Management scripts return XML rather than objects.</span></span> <span data-ttu-id="aa459-107">O XML não está em um formato legível.</span><span class="sxs-lookup"><span data-stu-id="aa459-107">The XML is not in a human-readable format.</span></span> <span data-ttu-id="aa459-108">Você pode usar os métodos da API do [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) e o arquivo XSL pré-instalado para transformar os dados no formato legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="aa459-108">You can use the methods of the [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API and the preinstalled XSL file to transform the data into human-readable format.</span></span>

<span data-ttu-id="aa459-109">Para obter mais informações sobre a saída XML do WinRM e exemplos de XML brutos e formatados, consulte [scripting in Gerenciamento remoto do Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="aa459-109">For more information about WinRM XML output and examples of raw and formatted XML, see [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="aa459-110">A ferramenta de linha de comando **WinRM** vem com um arquivo de transformação chamado WsmTxt. xsl que exibe a saída em um formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="aa459-110">The **Winrm** command-line tool comes with a transform file named WsmTxt.xsl that displays output in a tabular form.</span></span> <span data-ttu-id="aa459-111">Se o script fornecer esse arquivo para os métodos do MSXML que executam o transforma, a saída aparecerá da mesma forma que a saída da ferramenta **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="aa459-111">If your script supplies this file to the MSXML methods that perform tranforms, the output appears the same as the output from the **Winrm** tool.</span></span>

<span data-ttu-id="aa459-112">**Para formatar a saída XML bruta**</span><span class="sxs-lookup"><span data-stu-id="aa459-112">**To format raw XML output**</span></span>

1.  <span data-ttu-id="aa459-113">Crie o objeto [**WSMan**](wsman.md) e crie uma sessão.</span><span class="sxs-lookup"><span data-stu-id="aa459-113">Create the [**WSMan**](wsman.md) object and create a session.</span></span>

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  <span data-ttu-id="aa459-114">Crie objetos MSXML que representam a saída de resposta XML e a transformação XSL.</span><span class="sxs-lookup"><span data-stu-id="aa459-114">Create MSXML objects that represent the XML response output and the XSL transform.</span></span>

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  <span data-ttu-id="aa459-115">Obter dados por meio de métodos de objeto de [**sessão**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="aa459-115">Obtain data through [**Session**](session.md) object methods.</span></span>

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  <span data-ttu-id="aa459-116">Forneça a resposta para o método [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) do MSXML e o método [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) para armazenar o arquivo de transformação.</span><span class="sxs-lookup"><span data-stu-id="aa459-116">Supply the response to the MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) method and the [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) method to store the transform file.</span></span>

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  <span data-ttu-id="aa459-117">Use o método [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) do MSXML e exiba ou salve a saída.</span><span class="sxs-lookup"><span data-stu-id="aa459-117">Use the MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) method and display or save the output.</span></span>

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

<span data-ttu-id="aa459-118">O exemplo de código VBScript a seguir mostra o script completo.</span><span class="sxs-lookup"><span data-stu-id="aa459-118">The following VBScript code example shows the complete script.</span></span>


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a><span data-ttu-id="aa459-119">Adicionando uma sub-rotina portátil para transformar XML em seus scripts</span><span class="sxs-lookup"><span data-stu-id="aa459-119">Adding a Portable Subroutine to Transform XML to Your Scripts</span></span>

<span data-ttu-id="aa459-120">Você pode adicionar uma sub-rotina a seus scripts que usa o arquivo XSL pré-instalado para converter a saída XML bruta de um script do WinRM em um formulário tabular.</span><span class="sxs-lookup"><span data-stu-id="aa459-120">You can add a subroutine to your scripts that uses the preinstalled XSL file to convert the raw XML output from a WinRM script to a tabular form.</span></span>

<span data-ttu-id="aa459-121">A sub-rotina a seguir usa chamadas para os métodos de script MSXML para fornecer a saída para WsmTxt. Xsl.</span><span class="sxs-lookup"><span data-stu-id="aa459-121">The following subroutine uses calls to the MSXML scripting methods to supply the output to WsmTxt.xsl.</span></span>


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



<span data-ttu-id="aa459-122">A seguinte sub-rotina transforma cada linha de seus dados, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa459-122">The following subroutine transforms each line of your data as shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="aa459-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa459-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa459-124">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="aa459-124">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="aa459-125">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="aa459-125">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="aa459-126">Referência de Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="aa459-126">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 