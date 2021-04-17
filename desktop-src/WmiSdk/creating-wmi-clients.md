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
# <a name="creating-wmi-clients"></a>Criando clientes WMI

O WMI fornece uma infraestrutura de gerenciamento de sistema padronizada que pode ser utilizada por vários clientes diferentes. Esses clientes variam da ferramenta de linha de comando wmic.exe para System Center Operations Manager. Você pode escrever seus próprios clientes do WMI usando a API de script do WMI, a API C++ nativa ou usando os tipos no namespace System. Management .NET Framework Class Library.

## <a name="how-to-create-a-wmi-client"></a>Como criar um cliente WMI

A principal funcionalidade do WMI consiste em recuperar objetos do repositório do WMI e examinar as propriedades desses objetos. Você também pode optar por atualizar essas propriedades ou chamar métodos nessas propriedades. Os exemplos a seguir mostram como executar uma tarefa básica de administração do WMI: Recuperando o nome do computador local.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Termo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Criando um cliente com o PowerShell<br/></td>
<td>O WMI e o PowerShell estão totalmente integrados; assim, a recuperação de objetos WMI com o PowerShell é simplesmente uma questão de chamar o cmdlet Get-WmiObject. Observe que, para consistência, o primeiro trecho de código declara explicitamente muitos dos valores padrão; a segunda assume que os valores padrão estão corretos.<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Criando um cliente com o VBScript</p></td>
<td><p>O VBScript era a linguagem de script original que tinha uso comum com o WMI. Embora o PowerShell tenha se tornado mais popular, muitos dos exemplos de código existentes nesta documentação são escritos em VBScript. Observe que esse exemplo específico de VBScript declara explicitamente o caminho do computador local, bem como o nível de representação; Isso não é necessário, mas geralmente é uma prática recomendada.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Criando um cliente com C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</p></td>
<td><p>Esse namespace contém a solução atual para acessar o WMI com código gerenciado e é conhecido como Windows Management Infrastructure (MI ou WMIv2). Atualmente, MI é a tecnologia com suporte para a criação de clientes de gerenciamento gerenciado. Para obter mais informações, consulte <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">como implementar um cliente mi gerenciado</a> e <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">como implementar um cliente mi nativo</a>.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Criando um cliente com C# (<a href="/dotnet/api/system.management">System. Management</a>)</p></td>
<td><p>Esse namespace contém a solução original para acessar o WMI com código gerenciado. Embora as classes <a href="/dotnet/api/system.management">System. Management</a> ainda estejam disponíveis, as classes <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> são geralmente mais eficientes e dimensionadas melhor. Assim, é recomendável que você use as classes MI, em vez das classes WMI originais.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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



 

A tabela a seguir lista os tópicos abordados nesta seção.



| Tópico                                                                                                        | Descrição                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)                         | Descreve uma série de problemas que surgem quando os clientes usam a infraestrutura WMI em um computador remoto.                                                                                          |
| [Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)                         | Mostra o código de cliente WMI de exemplo.                                                                                                                                                                 |
| [Criando um script ou aplicativo WMI](creating-a-wmi-application-or-script.md)                             | Fornece informações sobre como criar vários clientes WMI.                                                                                                                                       |
| [Monitorando dados de desempenho](monitoring-performance-data.md)                                               | Descreve como usar o WMI para monitorar dados de desempenho.                                                                                                                                          |
| [Recebendo um evento WMI](receiving-a-wmi-event.md)                                                           | Descreve como exibir eventos WMI.                                                                                                                                                              |
| [Eventos de monitoramento](monitoring-events.md)                                                                   | Descreve como monitorar eventos WMI.                                                                                                                                                           |
| [Consultando com WQL](querying-with-wql.md)                                                                   | Apresenta o linguagem WQL (WQL).                                                                                                                                                       |
| [Consultando o status de recursos opcionais](querying-the-status-of-optional-features.md)                     | No Windows 7, a WMI implementou a classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Essa classe recupera o status dos recursos opcionais que estão presentes em um computador. |
| [Descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md)                       | Concentra-se na sintaxe para descrever o local de uma entidade gerenciada por WMI.                                                                                                                     |
| [Acessando outros recursos do sistema operacional com o WMI](accessing-other-operating-system-features-with-wmi.md) | Descreve como gravar clientes WMI que acessam drivers de dispositivo, Active Directory e dispositivos SNMP.                                                                                             |
| [Acessando dados no namespace Interop](accessing-data-in-the-interop-namespace.md)                       | Provedores de associação permitem que clientes Instrumentação de Gerenciamento do Windows (WMI) percorram e recuperem perfis e instâncias de classe associadas de namespaces diferentes.                      |
| [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md)               | Descreve as tarefas comuns que os clientes WMI devem executar.                                                                                                                                      |
| [Vinculando classes](linking-classes-together.md)                                                     | Discute o provedor de exibição e como ele pode ser usado para reunir informações de várias classes WMI.                                                                                    |
| [Modificando o registro do sistema](modifying-the-system-registry.md)                                           | Descreve como os clientes WMI podem usar o WMI para gerenciar informações de registro do sistema.                                                                                                                   |



 

