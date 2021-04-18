---
description: Para obter dados do WMI, seja no computador local ou em um computador remoto, você deve se conectar ao serviço WMI conectando-se a um namespace específico.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Tarefas do WMI: conectando-se ao serviço WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771552"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="28329-103">Tarefas do WMI: conectando-se ao serviço WMI</span><span class="sxs-lookup"><span data-stu-id="28329-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="28329-104">Para obter dados do WMI, seja no computador local ou em um computador remoto, você deve se conectar ao serviço WMI conectando-se a um [*namespace*](gloss-n.md)específico.</span><span class="sxs-lookup"><span data-stu-id="28329-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="28329-105">Na maioria dos casos, use a conexão de [moniker](creating-a-wmi-script.md) abreviada ou a conexão do [**localizador**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="28329-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="28329-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="28329-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="28329-107">As conexões remotas exigem configurações apropriadas para o Firewall do Windows e o DCOM.</span><span class="sxs-lookup"><span data-stu-id="28329-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="28329-108">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md) e [conectando por meio do firewall do Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="28329-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="28329-109">A partir do Windows Vista, o UAC (controle de conta de usuário) pode afetar o acesso WMI.</span><span class="sxs-lookup"><span data-stu-id="28329-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="28329-110">Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="28329-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="28329-111">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="28329-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="28329-112">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="28329-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="28329-113">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="28329-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="28329-114">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="28329-114">**To run a script**</span></span>

1.  <span data-ttu-id="28329-115">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="28329-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="28329-116">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="28329-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="28329-117">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="28329-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="28329-118">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="28329-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="28329-119">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="28329-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="28329-120">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="28329-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="28329-121">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="28329-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="28329-122">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="28329-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="28329-123">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="28329-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="28329-124">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="28329-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28329-125">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="28329-125">How do I...</span></span></th>
<th><span data-ttu-id="28329-126">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="28329-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28329-127">... conectar-se a um computador remoto usando o WMI?</span><span class="sxs-lookup"><span data-stu-id="28329-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="28329-128">Especifique um dos seguintes como parte da cadeia de conexão do <a href="constructing-a-moniker-string.md">moniker</a> :</span><span class="sxs-lookup"><span data-stu-id="28329-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="28329-129">Um nome de computador NetBIOS, como &quot; ATL-DC-01&quot;</span><span class="sxs-lookup"><span data-stu-id="28329-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="28329-130">Um nome de domínio totalmente qualificado, como &quot; ATL-DC-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="28329-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="28329-131">Um endereço IPv4, como &quot; 192.168.1.1&quot;</span><span class="sxs-lookup"><span data-stu-id="28329-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="28329-132">A partir do Windows Vista, você pode especificar um endereço IPv6 se o computador de destino e o computador do qual você está fazendo a conexão executarem o IPv6.</span><span class="sxs-lookup"><span data-stu-id="28329-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="28329-133">Para obter mais informações, consulte <a href="connecting-to-wmi-on-a-remote-computer.md">conectando-se ao WMI em um computador remoto</a> e <a href="ipv6-and-ipv4-support-in-wmi.md">suporte a IPv6 e IPv4 no WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="28329-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28329-134">VB</span><span class="sxs-lookup"><span data-stu-id="28329-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28329-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="28329-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="28329-136">... executar um script WMI em credenciais alternativas?</span><span class="sxs-lookup"><span data-stu-id="28329-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="28329-137">Use o método <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> ou <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator:: ConnectServer</strong></a> em C++ e inclua o nome de usuário e a senha apropriados.</span><span class="sxs-lookup"><span data-stu-id="28329-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="28329-138">Você não pode alterar credenciais ao se conectar ao computador local.</span><span class="sxs-lookup"><span data-stu-id="28329-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="28329-139">Para obter mais informações, consulte <a href="creating-a-wmi-script.md">criando um script WMI</a> e <a href="connecting-to-wmi-on-a-remote-computer.md">conectando-se ao WMI em um computador remoto</a>.</span><span class="sxs-lookup"><span data-stu-id="28329-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28329-140">VB</span><span class="sxs-lookup"><span data-stu-id="28329-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28329-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="28329-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="28329-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28329-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28329-143">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="28329-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="28329-144">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="28329-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="28329-145">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="28329-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
