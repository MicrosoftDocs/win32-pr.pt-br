---
description: Tarefas WMI para rede gerencie e obtenha informações sobre conexões e endereços IP ou MAC. Para obter outros exemplos, consulte o TechNet ScriptCenter em https://www.microsoft.com/technet .
ms.assetid: 25da32c3-34bf-4c88-9b09-ff371f2cf8db
ms.tgt_platform: multiple
title: 'Tarefas do WMI: rede'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31e8346a064fe2f6c7ab624897be8e789474f7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780694"
---
# <a name="wmi-tasks-networking"></a><span data-ttu-id="5a90e-104">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="5a90e-104">WMI Tasks: Networking</span></span>

<span data-ttu-id="5a90e-105">Tarefas WMI para rede gerencie e obtenha informações sobre conexões e endereços IP ou MAC.</span><span class="sxs-lookup"><span data-stu-id="5a90e-105">WMI tasks for networking manage and obtain information about connections and IP or MAC addresses.</span></span> <span data-ttu-id="5a90e-106">Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5a90e-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="5a90e-107">Os exemplos de script mostrados neste tópico obtêm dados somente do computador local.</span><span class="sxs-lookup"><span data-stu-id="5a90e-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="5a90e-108">Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="5a90e-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="5a90e-109">O procedimento a seguir descreve como executar um script.</span><span class="sxs-lookup"><span data-stu-id="5a90e-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="5a90e-110">**Para executar um script**</span><span class="sxs-lookup"><span data-stu-id="5a90e-110">**To run a script**</span></span>

1.  <span data-ttu-id="5a90e-111">Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="5a90e-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="5a90e-112">Verifique se o editor de texto não adiciona uma extensão. txt ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a90e-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="5a90e-113">Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a90e-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="5a90e-114">Digite **cscript filename.vbs** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="5a90e-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="5a90e-115">Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="5a90e-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="5a90e-116">Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).</span><span class="sxs-lookup"><span data-stu-id="5a90e-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="5a90e-117">Por padrão, o cscript exibe a saída de um script na janela de prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="5a90e-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="5a90e-118">Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a90e-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="5a90e-119">Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="5a90e-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="5a90e-120">A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.</span><span class="sxs-lookup"><span data-stu-id="5a90e-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-121">Como fazer...</span><span class="sxs-lookup"><span data-stu-id="5a90e-121">How do I...</span></span></th>
<th><span data-ttu-id="5a90e-122">Classes ou métodos WMI</span><span class="sxs-lookup"><span data-stu-id="5a90e-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a90e-123">... desabilitar uma conexão de rede usando o WMI?</span><span class="sxs-lookup"><span data-stu-id="5a90e-123">...disable a network connection using WMI?</span></span></td>
<td><span data-ttu-id="5a90e-124">Se você estiver usando DHCP, use o <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> para liberar o endereço IP.</span><span class="sxs-lookup"><span data-stu-id="5a90e-124">If you are using DHCP, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> and the <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> method to release the IP address.</span></span> <span data-ttu-id="5a90e-125">Se você não estiver usando o DHCP, não poderá usar o WMI para desabilitar uma conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="5a90e-125">If you are not using DHCP, you cannot use WMI to disable a network connection.</span></span> <span data-ttu-id="5a90e-126">Para reabilitar a conexão de rede, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard. RenewDHCPLease</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5a90e-126">To re-enable the network connection, use <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard.RenewDHCPLease</strong></a>.</span></span> <span data-ttu-id="5a90e-127">Você também pode liberar ou renovar todas as concessões de DHCP usando os métodos <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> e <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-127">You can also release or renew all of the DHCP leases using the <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> and <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> methods.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-128">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetCards = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration &quot; _
        & &quot;Where IPEnabled = True&quot;)
For Each objNetCard in colNetCards
    objNetCard.ReleaseDHCPLease()
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
<th><span data-ttu-id="5a90e-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a90e-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$net = Get-WMIObject -class Win32_NetworkAdapterConfiguration -ComputerName $computer
$netenabled = $net | where {$_.IPenabled}
foreach ($NetCard in $netenabled) {
    &quot;Releasing lease on: {0}&quot; -f $netcard.caption
 $netcard.ReleaseDHCPLease()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a90e-130">... desabilitar ou habilitar uma NIC?</span><span class="sxs-lookup"><span data-stu-id="5a90e-130">...disable or enable a NIC?</span></span></td>
<td><p><span data-ttu-id="5a90e-131">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> e os métodos <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> ou <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> or <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable</strong></a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a90e-132">... determinar qual endereço IP foi atribuído a uma determinada conexão de rede?</span><span class="sxs-lookup"><span data-stu-id="5a90e-132">...determine which IP address has been assigned to a given network connection?</span></span></td>
<td><p><span data-ttu-id="5a90e-133">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> e a propriedade <strong>NetConnectionID</strong> para determinar o endereço MAC da conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="5a90e-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> class and the <strong>NetConnectionID</strong> property to determine the MAC address of the network connection.</span></span> <span data-ttu-id="5a90e-134">Em seguida, use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> para localizar o endereço IP associado ao endereço Mac.</span><span class="sxs-lookup"><span data-stu-id="5a90e-134">Then, use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class to find the IP address associated with the MAC address.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-135">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection 2&#39;&quot;)

For Each objItem in colItems
    strMACAddress = objItem.MACAddress
Next

Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration&quot;)

For Each objItem in colItems
    If objItem.MACAddress = strMACAddress Then
        For Each strIPAddress in objItem.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-136">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNics = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection&#39;&quot;)
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      (&quot;ASSOCIATORS OF &quot; _
          & &quot;{Win32_NetworkAdapter.DeviceID=&#39;&quot; & _
      objNic.DeviceID & &quot;&#39;}&quot; & _
      &quot; WHERE AssocClass=Win32_NetworkAdapterSetting&quot;)
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a90e-137">... determinar o endereço MAC de um adaptador de rede?</span><span class="sxs-lookup"><span data-stu-id="5a90e-137">...determine the MAC address of a network adapter?</span></span></td>
<td><p><span data-ttu-id="5a90e-138">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e verifique o valor da propriedade <strong>MACAddress</strong> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>MACAddress</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a90e-139">... determinar o endereço IP de um computador?</span><span class="sxs-lookup"><span data-stu-id="5a90e-139">...determine the IP address of a computer?</span></span></td>
<td><p><span data-ttu-id="5a90e-140">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e verifique o valor da propriedade <strong>IPAddress</strong> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and check the value of the <strong>IPAddress</strong> property.</span></span> <span data-ttu-id="5a90e-141">Isso é retornado como uma matriz, portanto, use um loop For-Each para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="5a90e-141">This is returned as an array, so use a For-Each loop to get the value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-142">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration &quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
            to UBound(IPConfig.IPAddress)
                WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
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
<th><span data-ttu-id="5a90e-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a90e-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$IPconfigset = Get-WmiObject Win32_NetworkAdapterConfiguration
  
# Iterate and get IP address
$count = 0
foreach ($IPConfig in $IPConfigSet) {
   if ($Ipconfig.IPaddress) {
      foreach ($addr in $Ipconfig.Ipaddress) {
   &quot;IP Address   : {0}&quot; -f  $addr;
   $count++ 
   }
   }
}
if ($count -eq 0) {&quot;No IP addresses found&quot;}
else {&quot;$Count IP addresses found on this system&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a90e-144">...configlhar um computador para começar a obter seu endereço IP por meio do DHCP?</span><span class="sxs-lookup"><span data-stu-id="5a90e-144">...configure a computer to start getting its IP address through DHCP?</span></span></td>
<td><p><span data-ttu-id="5a90e-145">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-146">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-146">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
 
For Each objNetAdapter In colNetAdapters
    errEnable = objNetAdapter.EnableDHCP()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a90e-147">... atribuir um computador a um endereço IP estático?</span><span class="sxs-lookup"><span data-stu-id="5a90e-147">...assign a computer a static IP address?</span></span></td>
<td><p><span data-ttu-id="5a90e-148">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e o método <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-148">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-149">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-149">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
strIPAddress = Array(&quot;192.168.1.141&quot;)
strSubnetMask = Array(&quot;255.255.255.0&quot;)
strGateway = Array(&quot;192.168.1.100&quot;)
strGatewayMetric = Array(1)
 
For Each objNetAdapter in colNetAdapters
    errEnable = objNetAdapter.EnableStatic( _
        strIPAddress, strSubnetMask)
    errGateways = objNetAdapter.SetGateways(_
        strGateway, strGatewaymetric)
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a90e-150">... obter informações sobre adaptadores de rede sem recuperar também informações sobre tarefas como conexões RAS e VPN?</span><span class="sxs-lookup"><span data-stu-id="5a90e-150">...get information about network adapters without also retrieving information about things like RAS and VPN connections?</span></span></td>
<td><p><span data-ttu-id="5a90e-151">Use a classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> class.</span></span> <span data-ttu-id="5a90e-152">Em sua consulta <a href="querying-with-wql.md">WQL</a> , use esta cláusula: Where <strong>IPEnabled</strong>  =  <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="5a90e-152">In your <a href="querying-with-wql.md">WQL</a> query, use this clause: Where <strong>IPEnabled</strong> = <strong>True</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-153">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-153">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration&quot; _
        & &quot; where IPEnabled=TRUE&quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
        to UBound(IPConfig.IPAddress)
            WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a90e-154">... executar ping em um computador sem usar Ping.exe?</span><span class="sxs-lookup"><span data-stu-id="5a90e-154">...ping a computer without using Ping.exe?</span></span></td>
<td><p><span data-ttu-id="5a90e-155">Use a classe <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5a90e-155">Use the <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> class.</span></span></p>
<p><span data-ttu-id="5a90e-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> pode retornar dados para computadores que têm endereços IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="5a90e-156"><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> can return data for computers that have both IPv4 addresses and IPv6 addresses.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-157">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPings = objWMIService.ExecQuery _
    (&quot;Select * From Win32_PingStatus where Address = &#39;192.168.1.1&#39;&quot;)

For Each objStatus in colPings
    If IsNull(objStatus.StatusCode) _
        or objStatus.StatusCode<>0 Then 
        WScript.Echo &quot;Computer did not respond.&quot; 
    Else
        Wscript.Echo &quot;Computer responded.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a90e-158">VB</span><span class="sxs-lookup"><span data-stu-id="5a90e-158">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;client1&quot;
Set objShell = CreateObject(&quot;WScript.Shell&quot;)
Set objScriptExec = objShell.Exec( _
    &quot;ping -n 2 -w 1000 &quot; & strComputer)
strPingResults = LCase(objScriptExec.StdOut.ReadAll)
If InStr(strPingResults, &quot;reply from&quot;) Then
    If InStr(strPingResults, &quot;destination net unreachable&quot;) Then
        WScript.Echo strComputer & &quot;did not respond to ping.&quot;
    Else
        WScript.Echo strComputer & &quot; responded to ping.&quot;
    End If 
Else
    WScript.Echo strComputer & &quot; did not respond to ping.&quot;
End If
  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5a90e-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a90e-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a90e-160">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="5a90e-160">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="5a90e-161">Exemplos de aplicativos WMI C++</span><span class="sxs-lookup"><span data-stu-id="5a90e-161">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="5a90e-162">ScriptCenter do TechNet</span><span class="sxs-lookup"><span data-stu-id="5a90e-162">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

