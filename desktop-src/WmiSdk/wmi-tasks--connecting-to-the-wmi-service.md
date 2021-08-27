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
ms.openlocfilehash: 4da816b45709f6140efb7e6e0460e27d9f9ed00f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627712"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>Tarefas do WMI: conectando-se ao serviço WMI

Para obter dados do WMI, seja no computador local ou em um computador remoto, você deve se conectar ao serviço WMI conectando-se a um [*namespace*](gloss-n.md)específico. Na maioria dos casos, use a conexão de [moniker](creating-a-wmi-script.md) abreviada ou a conexão do [**localizador**](swbemlocator-connectserver.md) . Para obter outros exemplos, consulte o TechNet ScriptCenter em [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

as conexões remotas exigem configurações apropriadas para o Firewall Windows e o DCOM. para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md) e [conectando por meio do Firewall Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). a partir do Windows Vista, o UAC (controle de conta de usuário) pode afetar o acesso WMI. Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

Os exemplos de script mostrados neste tópico obtêm dados somente do computador local. Para obter mais informações sobre como usar o script para obter dados de computadores remotos, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).


O procedimento a seguir descreve como executar um script.

**Para executar um script**

1.  Copie o código e salve-o em um arquivo com uma extensão. vbs, como *filename.vbs*. Verifique se o editor de texto não adiciona uma extensão de .txt ao arquivo.
2.  Abra uma janela de prompt de comando e navegue até o diretório em que você salvou o arquivo.
3.  Digite **cscript filename.vbs** no prompt de comando.
4.  Se você não puder acessar um log de eventos, verifique se você está executando a partir de um prompt de comandos com privilégios elevados. Alguns logs de eventos, como o log de eventos de segurança, podem ser protegidos por UAC (controles de acesso do usuário).

> [!Note]  
> Por padrão, o cscript exibe a saída de um script na janela de prompt de comando. Como os scripts WMI podem produzir grandes quantidades de saída, convém redirecionar a saída para um arquivo. Digite **cscript filename.vbs > outfile.txt** no prompt de comando para redirecionar a saída do script de *filename.vbs* para *outfile.txt*.

 

A tabela a seguir lista os exemplos de script que podem ser usados para obter vários tipos de dados do computador local.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Como fazer...</th>
<th>Classes ou métodos WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... conectar-se a um computador remoto usando o WMI?</td>
<td>Especifique um dos seguintes como parte da cadeia de conexão do <a href="constructing-a-moniker-string.md">moniker</a> :<br/>
<ul>
<li>Um nome de computador NetBIOS, como &quot; ATL-DC-01&quot;</li>
<li>Um nome de domínio totalmente qualificado, como &quot; ATL-DC-01.fabrikam.com&quot;</li>
<li>Um endereço IPv4, como &quot; 192.168.1.1&quot;</li>
<li>a partir do Windows Vista, você pode especificar um endereço ipv6 se o computador de destino e o computador do qual você está fazendo a conexão executarem o IPv6.<br/></li>
</ul>
Para obter mais informações, consulte <a href="connecting-to-wmi-on-a-remote-computer.md">conectando-se ao WMI em um computador remoto</a> e <a href="ipv6-and-ipv4-support-in-wmi.md">suporte a IPv6 e IPv4 no WMI</a>.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td>... executar um script WMI em credenciais alternativas?</td>
<td><p>Use o método <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> ou <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator:: ConnectServer</strong></a> em C++ e inclua o nome de usuário e a senha apropriados. Você não pode alterar credenciais ao se conectar ao computador local. Para obter mais informações, consulte <a href="creating-a-wmi-script.md">criando um script WMI</a> e <a href="connecting-to-wmi-on-a-remote-computer.md">conectando-se ao WMI em um computador remoto</a>.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do WMI para scripts e aplicativos](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Exemplos de aplicativos WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[ScriptCenter do TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
