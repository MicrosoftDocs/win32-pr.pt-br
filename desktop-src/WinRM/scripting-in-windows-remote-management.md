---
title: Criando scripts no Gerenciamento Remoto do Windows
description: A API de script no WinRM e a API COM de acompanhamento para C++ são projetadas para refletir de forma semelhante as operações do protocolo WS-Management.
ms.assetid: fda2042a-8fca-4cd8-bb55-fd1c3591921e
ms.tgt_platform: multiple
keywords:
- Criando scripts no Gerenciamento Remoto do Windows
- Gerenciamento Remoto do Windows, scripts em
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 75af10fea03853de99c884eda0a74ce340683b49
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084561"
---
# <a name="scripting-in-windows-remote-management"></a><span data-ttu-id="82565-105">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="82565-105">Scripting in Windows Remote Management</span></span>

<span data-ttu-id="82565-106">A [API de script no WinRM](winrm-scripting-api.md) e a API com de acompanhamento para C++ são projetadas para refletir de forma semelhante as operações do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="82565-106">The [Scripting API in WinRM](winrm-scripting-api.md) and the accompanying COM API for C++ are designed to closely reflect the operations of the WS-Management protocol.</span></span>

<span data-ttu-id="82565-107">A API de script do WinRM no Gerenciamento Remoto do Windows dá suporte a todas as operações de protocolo WS-Management, exceto uma.</span><span class="sxs-lookup"><span data-stu-id="82565-107">The WinRM Scripting API in Windows Remote Management supports all the WS-Management protocol operations except one.</span></span> <span data-ttu-id="82565-108">Ele não permite assinaturas para eventos.</span><span class="sxs-lookup"><span data-stu-id="82565-108">It does not allow subscriptions to events.</span></span> <span data-ttu-id="82565-109">Para assinar eventos do log de eventos do sistema BMC, você deve usar as ferramentas de linha de comando wecutil ou wevtutil.</span><span class="sxs-lookup"><span data-stu-id="82565-109">To subscribe to events from the BMC System Event Log, you must use the Wecutil or Wevtutil command-line tools.</span></span> <span data-ttu-id="82565-110">Para obter mais informações, consulte [Eventos](events.md).</span><span class="sxs-lookup"><span data-stu-id="82565-110">For more information, see [Events](events.md).</span></span>

<span data-ttu-id="82565-111">A API de script do WinRM é chamada pelo Winrm.vbs, uma ferramenta de linha de comando, que é escrita em Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="82565-111">The WinRM Scripting API is called by Winrm.vbs, a command-line tool, which is written in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="82565-112">Winrm.vbs fornece exemplos de como usar a [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="82565-112">Winrm.vbs provides examples of how to use the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

## <a name="using-wsman-compared-to-using-wmi-scripting"></a><span data-ttu-id="82565-113">Usando WSman comparado ao uso de scripts WMI</span><span class="sxs-lookup"><span data-stu-id="82565-113">Using WSman Compared to Using WMI Scripting</span></span>

<span data-ttu-id="82565-114">O WMI se conecta a computadores remotos por meio do DCOM, que requer a configuração descrita em [conectando-se ao WMI em um computador remoto](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="82565-114">WMI connects to remote computers through DCOM, which requires the configuration described in [Connecting to WMI on a Remote Computer](/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer).</span></span> <span data-ttu-id="82565-115">O WinRM não usa DCOM para se conectar a um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="82565-115">WinRM does not use DCOM to connect to a remote computer.</span></span> <span data-ttu-id="82565-116">Em vez disso, o protocolo WS-Management envia mensagens SOAP e o serviço usa uma única porta para HTTP e uma porta para transporte HTTPS.</span><span class="sxs-lookup"><span data-stu-id="82565-116">Instead, the WS-Management protocol sends SOAP messages and the service uses a single port for HTTP and a port for HTTPS transport.</span></span>

<span data-ttu-id="82565-117">Ao contrário da ferramenta de linha de comando do **WinRM** , os scripts devem fornecer o XML necessário para passar para as mensagens do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="82565-117">Unlike the **winrm** command-line tool, scripts must provide the XML required to pass to the WS-Management protocol messages.</span></span> <span data-ttu-id="82565-118">Eles também devem fornecer URIs.</span><span class="sxs-lookup"><span data-stu-id="82565-118">They must also provide URIs.</span></span> <span data-ttu-id="82565-119">Para obter mais informações, consulte [URIs de recurso](resource-uris.md) e [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="82565-119">For more information, see [Resource URIs](resource-uris.md) and [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="82565-120">A API de script WMI funciona com objetos, como instâncias de disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), que representam recursos em um computador.</span><span class="sxs-lookup"><span data-stu-id="82565-120">The WMI Scripting API works with objects, such as instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which represent resources on a computer.</span></span> <span data-ttu-id="82565-121">Essa classe WMI é definida em arquivos [*formato MOF (MOF)*](/windows/desktop/WmiSdk/gloss-m) , que são armazenados em formato binário no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="82565-121">This WMI class is defined in [*Managed Object Format (MOF)*](/windows/desktop/WmiSdk/gloss-m) files, which are stored in binary form in the WMI repository.</span></span> <span data-ttu-id="82565-122">No WMI, uma operação get para um único recurso ou uma consulta para várias instâncias retorna objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="82565-122">In WMI, a Get operation for a single resource or a query for multiple instances returns WMI objects.</span></span>

<span data-ttu-id="82565-123">Um script WinRM não retorna objetos, mas sim fluxos de texto XML.</span><span class="sxs-lookup"><span data-stu-id="82565-123">A WinRM script does not return objects, but rather streams of XML text.</span></span> <span data-ttu-id="82565-124">Para obter mais informações, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="82565-124">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="displaying-xml-output-from-winrm-scripts"></a><span data-ttu-id="82565-125">Exibindo a saída XML de scripts do WinRM</span><span class="sxs-lookup"><span data-stu-id="82565-125">Displaying XML Output from WinRM Scripts</span></span>

<span data-ttu-id="82565-126">A API de script do WinRM Obtém e recebe cadeias de caracteres XML que descrevem os recursos.</span><span class="sxs-lookup"><span data-stu-id="82565-126">The WinRM Scripting API gets and receives XML strings that describe resources.</span></span> <span data-ttu-id="82565-127">O XML resultante está na forma de um fluxo de texto e requer que uma transformação XML seja exibida de alguma outra maneira.</span><span class="sxs-lookup"><span data-stu-id="82565-127">The resultant XML is in the form of a text stream and requires an XML transform to be displayed in some other way.</span></span>

<span data-ttu-id="82565-128">O script WinRM a seguir produz saída XML bruta.</span><span class="sxs-lookup"><span data-stu-id="82565-128">The following WinRM script produces raw XML output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSxml.DOMDocument")
Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xmlFile.Save( "c:\RawOutput.xml")
```



<span data-ttu-id="82565-129">O bloco de texto a seguir mostra a saída XML do script do WinRM.</span><span class="sxs-lookup"><span data-stu-id="82565-129">The following block of text shows the XML output from the WinRM script.</span></span>


```XML
<p:Win32_Service xmlns:xsi="https://www.w3.org/2001/XMLSchema-
instance" xmlns:p="http://schemas.microsoft.com/wbem/wsman/1
/wmi/root/cimv2/Win32_Service" xmlns:cim="https://schemas.dmtf
.org/wbem/wsman/1/base" cim:Class="Win32_Service"><p:AcceptP
ause>false</p:AcceptPause><p:AcceptStop>true</p:AcceptStop>
<p:Caption>Print Spooler</p:Caption><p:CheckPoint>0</p:CheckP
oint><p:CreationClassName>Win32_Service</p:CreationClassName>
<p:Description>Loads files to memory for later printing</p:De
scription><p:DesktopInteract>true</p:DesktopInteract><p:Displ
ayName>Print Spooler</p:DisplayName><p:ErrorControl>Normal</p
:ErrorControl><p:ExitCode>0</p:ExitCode><p:InstallDate xsi:ni
l="true"/><p:Name>spooler</p:Name><p:PathName>C:\Windows\Syst
em32\spoolsv.exe</p:PathName><p:ProcessId>1720</p:ProcessId><
p:ServiceSpecificExitCode>0</p:ServiceSpecificExitCode><p:Ser
viceType>Own Process</p:ServiceType><p:Started>true</p:Starte
d><p:StartMode>Auto</p:StartMode><p:StartName>LocalSystem</p:
StartName><p:State>Running</p:State><p:Status>OK</p:Status><p
:SystemCreationClassName>Win32_ComputerSystem</p:SystemCreati
onClassName><p:SystemName>wsplab6-4</p:SystemName><p:TagId>0<
/p:TagId><p:WaitHint>0</p:WaitHint><cim:Location xmlns:cim="h
ttp://schemas.dmtf.org/wbem/wsman/1/base" xmlns:a="https://sc
hemas.xmlsoap.org/ws/2004/08/addressing" xmlns:w="https://sche
mas.dmtf.org/wbem/wsman/1/wsman"><a:Address>https://schemas.xm
lsoap.org/ws/2004/08/addressing/role/anonymous</a:Address><a:
ReferenceParameters><w:ResourceURI>https://schemas.microsoft.c
om/wbem/wsman/1/wmi/root/cimv2/Win32_Service</w:ResourceURI><
w:SelectorSet><w:Selector Name="Name">spooler</w:Selector></w
:SelectorSet></a:ReferenceParameters></cim:Location></p:Win32
_Service>
```



<span data-ttu-id="82565-130">Seus scripts podem usar uma transformação XML para tornar essa saída mais legível.</span><span class="sxs-lookup"><span data-stu-id="82565-130">Your scripts can use an XML transform to make this output more readable.</span></span> <span data-ttu-id="82565-131">Para obter mais informações, consulte [exibindo a saída XML de scripts do WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="82565-131">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>

<span data-ttu-id="82565-132">A seguinte versão do script formata o XML para a saída legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="82565-132">The following version of the script formats the XML into human-readable output.</span></span>


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

Set Session = Wsman.CreateSession
Response = Session.Get("http://schemas.microsoft.com/wbem/wsman/" _
    & "1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(Response)
xslFile.Load( "WsmTxt.xsl" )
Wscript.Echo xmlFile.TransformNode( xslFile )
```



<span data-ttu-id="82565-133">A transformação XSL cria a saída a seguir.</span><span class="sxs-lookup"><span data-stu-id="82565-133">The XSL transform creates the following output.</span></span>


```XML
Win32_Service
    AcceptPause = false
    AcceptStop = true
    Caption = Print Spooler
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = Loads files to memory for later printing
    DesktopInteract = true
    DisplayName = Print Spooler
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = Spooler
    PathName = C:\Windows\System32\spoolsv.exe
    ProcessId = 1720
    ServiceSpecificExitCode = 0
    ServiceType = Own Process
    Started = true
    StartMode = Auto
    StartName = LocalSystem
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = wsplab6-4
    TagId = 0
    WaitHint = 0
```



## <a name="winrm-script-and-winrmcmd-output"></a><span data-ttu-id="82565-134">Script do WinRM e a saída de WinRM. cmd</span><span class="sxs-lookup"><span data-stu-id="82565-134">WinRM Script and Winrm.cmd Output</span></span>

<span data-ttu-id="82565-135">A saída de um script do WinRM é codificada em Unicode.</span><span class="sxs-lookup"><span data-stu-id="82565-135">The output from a WinRM script is encoded in Unicode.</span></span> <span data-ttu-id="82565-136">Se você criar um [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) e gravar um arquivo do script, o arquivo resultante será Unicode.</span><span class="sxs-lookup"><span data-stu-id="82565-136">If you create a [FileSystemObject](/previous-versions//6kxy1a51(v=vs.85)) and write a file from the script, the resulting file is Unicode.</span></span> <span data-ttu-id="82565-137">No entanto, se você redirecionar a saída para um arquivo, a codificação será ANSI.</span><span class="sxs-lookup"><span data-stu-id="82565-137">However, if you redirect the output to a file, the encoding is ANSI.</span></span> <span data-ttu-id="82565-138">Se você redirecionar a saída para um arquivo XML e houver caracteres Unicode na saída, o XML será inválido.</span><span class="sxs-lookup"><span data-stu-id="82565-138">If you redirect the output to an XML file and there are Unicode characters in the output, the XML will be invalid.</span></span> <span data-ttu-id="82565-139">Lembre-se de que a ferramenta de linha de comando **WinRM** gera ANSI.</span><span class="sxs-lookup"><span data-stu-id="82565-139">Be aware that the **Winrm** command-line tool outputs ANSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82565-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82565-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82565-141">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="82565-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="82565-142">Usando Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="82565-142">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

<span data-ttu-id="82565-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82565-143">[MSXSL](/previous-versions/windows/desktop/ms763742(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="82565-144">[Referência do DOM](/previous-versions/windows/desktop/ms764730(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="82565-144">[DOM Reference](/previous-versions/windows/desktop/ms764730(v=vs.85))</span></span>
</dt> </dl>

 

 