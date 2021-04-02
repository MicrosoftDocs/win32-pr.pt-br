---
description: Os scripts WMI podem condensar muitas das etapas necessárias em um programa C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Conectando-se ao WMI com o VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829278"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="43779-103">Conectando-se ao WMI com o VBScript</span><span class="sxs-lookup"><span data-stu-id="43779-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="43779-104">Os scripts WMI podem condensar muitas das etapas necessárias em um programa C++.</span><span class="sxs-lookup"><span data-stu-id="43779-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="43779-105">Eles podem se conectar ao WMI, não apenas por meio de um objeto [**SWbemLocator**](swbemlocator.md) , mas também pelo moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="43779-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="43779-106">Um moniker é um nome curto que localiza um namespace, uma classe ou uma instância no WMI.</span><span class="sxs-lookup"><span data-stu-id="43779-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="43779-107">O nome "winmgmts:" é o moniker WMI que informa ao host de scripts do Windows para usar os objetos WMI, conecta-se ao namespace padrão e Obtém um objeto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="43779-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="43779-108">Outras informações de conexão, como um nível de representação ou uma classe ou instância específica, aparecem na cadeia de caracteres após o nome do moniker.</span><span class="sxs-lookup"><span data-stu-id="43779-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="43779-109">Você pode usar monikers em chamadas que criam ou obtêm objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="43779-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="43779-110">Para obter mais informações, consulte [construindo uma cadeia de caracteres de moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="43779-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="43779-111">O procedimento a seguir descreve como se conectar ao WMI usando o **SWbemLocator**.</span><span class="sxs-lookup"><span data-stu-id="43779-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="43779-112">**Para se conectar ao WMI usando o SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="43779-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="43779-113">Recupere um objeto do localizador com uma chamada para [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43779-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="43779-114">Faça logon no namespace usando uma chamada para o método [**ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="43779-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="43779-115">Se você não especificar um computador na chamada para [**ConnectServer**](swbemlocator-connectserver.md), o WMI se conectará ao computador local.</span><span class="sxs-lookup"><span data-stu-id="43779-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="43779-116">Se você não especificar um namespace, o WMI se conectará ao namespace especificado na chave do registro.</span><span class="sxs-lookup"><span data-stu-id="43779-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="43779-117">**HKEY \_ \_** \\  \\ Namespace padrão do software do computador local **Microsoft** \\ **WBEM** \\ **scripting** \\ </span><span class="sxs-lookup"><span data-stu-id="43779-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="43779-118">O namespace padrão é \\ raiz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="43779-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="43779-119">Para obter mais informações sobre namespaces, consulte [Criando hierarquias dentro do WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="43779-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="43779-120">Defina o nível de representação com uma chamada para o método [**SWbemServices \_ . Security**](swbemservices-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="43779-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="43779-121">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="43779-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="43779-122">Implemente a finalidade do seu script.</span><span class="sxs-lookup"><span data-stu-id="43779-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="43779-123">O WMI expõe uma variedade de objetos de script que usam o para acessar e manipular dados em toda a sua rede.</span><span class="sxs-lookup"><span data-stu-id="43779-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="43779-124">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e [API de script para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="43779-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

<span data-ttu-id="43779-125">O procedimento a seguir descreve como se conectar ao WMI e recuperar um objeto usando um moniker.</span><span class="sxs-lookup"><span data-stu-id="43779-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="43779-126">**Para se conectar ao WMI e recuperar um objeto usando um moniker**</span><span class="sxs-lookup"><span data-stu-id="43779-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="43779-127">Chame [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) com um moniker no parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="43779-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="43779-128">O moiniker contém vários elementos que você pode usar para se conectar ao WMI:</span><span class="sxs-lookup"><span data-stu-id="43779-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="43779-129">O "winmgmts:" informa ao WSH para usar [objetos de API de script](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="43779-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="43779-130">Neste exemplo específico, o WSH saberá que ele deve retornar um SWbemObject que descreve o primeiro scheduledJob Win32 \_ no sistema.</span><span class="sxs-lookup"><span data-stu-id="43779-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="43779-131">Outros objetos possíveis a serem retornados seriam um objeto SWbemCollection ou [**SWbemServices**](swbemservices.md) , dependendo do que o moniker descreveu.</span><span class="sxs-lookup"><span data-stu-id="43779-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="43779-132">Opcionalmente, você pode definir os níveis de segurança para a conexão.</span><span class="sxs-lookup"><span data-stu-id="43779-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="43779-133">Observe que você não pode definir informações de nome e senha em um moniker, no entanto.</span><span class="sxs-lookup"><span data-stu-id="43779-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="43779-134">Para obter mais informações, consulte [protegendo clientes de script](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="43779-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="43779-135">Opcionalmente, você pode definir o caminho para o objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="43779-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="43779-136">Isso inclui o computador local ou remoto, o namespace, bem como o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="43779-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="43779-137">Para obter mais informações sobre como usar o VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) em scripts WMI, consulte [criando uma instância](creating-an-instance.md) e [recuperando uma instância do WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="43779-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="43779-138">Em vez de recuperar um único item ou uma coleção, você também pode optar por recuperar o objeto [**SWbemServices**](swbemservices.md) (conforme descrito no exemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="43779-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="43779-139">Posteriormente, você pode chamar consultas adicionais no objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="43779-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="43779-140">No exemplo anterior, Impersonate ou impersonationLevel = 3 é o nível de segurança do processo padrão.</span><span class="sxs-lookup"><span data-stu-id="43779-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="43779-141">No exemplo a seguir, não é necessário especificar esse nível de segurança do processo, a menos que você precise alterar a segurança do processo para **delegar**.</span><span class="sxs-lookup"><span data-stu-id="43779-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="43779-142">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="43779-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43779-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43779-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43779-144">Scripts no WMI</span><span class="sxs-lookup"><span data-stu-id="43779-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
