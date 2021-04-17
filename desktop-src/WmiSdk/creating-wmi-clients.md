---
description: O WMI fornece uma infraestrutura de gerenciamento de sistema padronizada que pode ser utilizada por vários clientes diferentes.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Criando clientes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764261"
---
# <a name="creating-wmi-clients"></a><span data-ttu-id="78882-103">Criando clientes WMI</span><span class="sxs-lookup"><span data-stu-id="78882-103">Creating WMI Clients</span></span>

<span data-ttu-id="78882-104">O WMI fornece uma infraestrutura de gerenciamento de sistema padronizada que pode ser utilizada por vários clientes diferentes.</span><span class="sxs-lookup"><span data-stu-id="78882-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="78882-105">Esses clientes variam da ferramenta de linha de comando wmic.exe para System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="78882-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="78882-106">Você pode escrever seus próprios clientes do WMI usando a API de script do WMI, a API C++ nativa ou usando os tipos no namespace System. Management .NET Framework Class Library.</span><span class="sxs-lookup"><span data-stu-id="78882-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="78882-107">Como criar um cliente WMI</span><span class="sxs-lookup"><span data-stu-id="78882-107">How to create a WMI client</span></span>

<span data-ttu-id="78882-108">A principal funcionalidade do WMI consiste em recuperar objetos do repositório do WMI e examinar as propriedades desses objetos.</span><span class="sxs-lookup"><span data-stu-id="78882-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="78882-109">Você também pode optar por atualizar essas propriedades ou chamar métodos nessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="78882-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="78882-110">Os exemplos a seguir mostram como executar uma tarefa básica de administração do WMI: Recuperando o nome do computador local.</span><span class="sxs-lookup"><span data-stu-id="78882-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78882-111">Termo</span><span class="sxs-lookup"><span data-stu-id="78882-111">Term</span></span></th>
<th><span data-ttu-id="78882-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="78882-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78882-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Criando um cliente com o PowerShell</span><span class="sxs-lookup"><span data-stu-id="78882-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="78882-114">O WMI e o PowerShell estão totalmente integrados; assim, a recuperação de objetos WMI com o PowerShell é simplesmente uma questão de chamar o cmdlet Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="78882-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="78882-115">Observe que, para consistência, o primeiro trecho de código declara explicitamente muitos dos valores padrão; a segunda assume que os valores padrão estão corretos.</span><span class="sxs-lookup"><span data-stu-id="78882-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78882-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="78882-116">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78882-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Criando um cliente com o VBScript</span><span class="sxs-lookup"><span data-stu-id="78882-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="78882-118">O VBScript era a linguagem de script original que tinha uso comum com o WMI.</span><span class="sxs-lookup"><span data-stu-id="78882-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="78882-119">Embora o PowerShell tenha se tornado mais popular, muitos dos exemplos de código existentes nesta documentação são escritos em VBScript.</span><span class="sxs-lookup"><span data-stu-id="78882-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="78882-120">Observe que esse exemplo específico de VBScript declara explicitamente o caminho do computador local, bem como o nível de representação; Isso não é necessário, mas geralmente é uma prática recomendada.</span><span class="sxs-lookup"><span data-stu-id="78882-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78882-121">VB</span><span class="sxs-lookup"><span data-stu-id="78882-121">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78882-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Criando um cliente com C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</span><span class="sxs-lookup"><span data-stu-id="78882-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="78882-123">Esse namespace contém a solução atual para acessar o WMI com código gerenciado e é conhecido como Windows Management Infrastructure (MI ou WMIv2).</span><span class="sxs-lookup"><span data-stu-id="78882-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="78882-124">Atualmente, MI é a tecnologia com suporte para a criação de clientes de gerenciamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="78882-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="78882-125">Para obter mais informações, consulte <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">como implementar um cliente mi gerenciado</a> e <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">como implementar um cliente mi nativo</a>.</span><span class="sxs-lookup"><span data-stu-id="78882-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78882-126">C#</span><span class="sxs-lookup"><span data-stu-id="78882-126">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78882-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Criando um cliente com C# (<a href="/dotnet/api/system.management">System. Management</a>)</span><span class="sxs-lookup"><span data-stu-id="78882-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="78882-128">Esse namespace contém a solução original para acessar o WMI com código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="78882-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="78882-129">Embora as classes <a href="/dotnet/api/system.management">System. Management</a> ainda estejam disponíveis, as classes <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> são geralmente mais eficientes e dimensionadas melhor.</span><span class="sxs-lookup"><span data-stu-id="78882-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="78882-130">Assim, é recomendável que você use as classes MI, em vez das classes WMI originais.</span><span class="sxs-lookup"><span data-stu-id="78882-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78882-131">C#</span><span class="sxs-lookup"><span data-stu-id="78882-131">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="78882-132">A tabela a seguir lista os tópicos abordados nesta seção.</span><span class="sxs-lookup"><span data-stu-id="78882-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="78882-133">Tópico</span><span class="sxs-lookup"><span data-stu-id="78882-133">Topic</span></span>                                                                                                        | <span data-ttu-id="78882-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="78882-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78882-135">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="78882-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="78882-136">Descreve uma série de problemas que surgem quando os clientes usam a infraestrutura WMI em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="78882-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="78882-137">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="78882-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="78882-138">Mostra o código de cliente WMI de exemplo.</span><span class="sxs-lookup"><span data-stu-id="78882-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="78882-139">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="78882-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="78882-140">Fornece informações sobre como criar vários clientes WMI.</span><span class="sxs-lookup"><span data-stu-id="78882-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="78882-141">Monitorando dados de desempenho</span><span class="sxs-lookup"><span data-stu-id="78882-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="78882-142">Descreve como usar o WMI para monitorar dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="78882-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="78882-143">Recebendo um evento WMI</span><span class="sxs-lookup"><span data-stu-id="78882-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="78882-144">Descreve como exibir eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="78882-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="78882-145">Eventos de monitoramento</span><span class="sxs-lookup"><span data-stu-id="78882-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="78882-146">Descreve como monitorar eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="78882-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="78882-147">Consultando com WQL</span><span class="sxs-lookup"><span data-stu-id="78882-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="78882-148">Apresenta o linguagem WQL (WQL).</span><span class="sxs-lookup"><span data-stu-id="78882-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="78882-149">Consultando o status de recursos opcionais</span><span class="sxs-lookup"><span data-stu-id="78882-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="78882-150">No Windows 7, a WMI implementou a classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="78882-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="78882-151">Essa classe recupera o status dos recursos opcionais que estão presentes em um computador.</span><span class="sxs-lookup"><span data-stu-id="78882-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="78882-152">Descrevendo o local de um objeto WMI</span><span class="sxs-lookup"><span data-stu-id="78882-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="78882-153">Concentra-se na sintaxe para descrever o local de uma entidade gerenciada por WMI.</span><span class="sxs-lookup"><span data-stu-id="78882-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="78882-154">Acessando outros recursos do sistema operacional com o WMI</span><span class="sxs-lookup"><span data-stu-id="78882-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="78882-155">Descreve como gravar clientes WMI que acessam drivers de dispositivo, Active Directory e dispositivos SNMP.</span><span class="sxs-lookup"><span data-stu-id="78882-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="78882-156">Acessando dados no namespace Interop</span><span class="sxs-lookup"><span data-stu-id="78882-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="78882-157">Provedores de associação permitem que clientes Instrumentação de Gerenciamento do Windows (WMI) percorram e recuperem perfis e instâncias de classe associadas de namespaces diferentes.</span><span class="sxs-lookup"><span data-stu-id="78882-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="78882-158">Manipulando informações de classe e instância</span><span class="sxs-lookup"><span data-stu-id="78882-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="78882-159">Descreve as tarefas comuns que os clientes WMI devem executar.</span><span class="sxs-lookup"><span data-stu-id="78882-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="78882-160">Vinculando classes</span><span class="sxs-lookup"><span data-stu-id="78882-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="78882-161">Discute o provedor de exibição e como ele pode ser usado para reunir informações de várias classes WMI.</span><span class="sxs-lookup"><span data-stu-id="78882-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="78882-162">Modificando o registro do sistema</span><span class="sxs-lookup"><span data-stu-id="78882-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="78882-163">Descreve como os clientes WMI podem usar o WMI para gerenciar informações de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="78882-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

