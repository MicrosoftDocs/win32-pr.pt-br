---
description: Descreve como scripts, aplicativos e provedores podem estabelecer conexões com o WMI em computadores remotos para obter dados ou controlar hardware e software.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Conectando-se ao WMI em um computador remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759525"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Conectando-se ao WMI em um computador remoto

O WMI pode ser usado para gerenciar e acessar dados do WMI em computadores remotos. As conexões remotas no WMI são afetadas pelo [Firewall do Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) e pelas configurações do DCOM. O [UAC (controle de conta de usuário)](/previous-versions/aa905108(v=msdn.10)) também pode exigir alterações em algumas configurações. No entanto, depois que suas configurações estiverem corretas, a chamada para um sistema remoto será muito semelhante a uma chamada de WMI local. Você pode optar por torná-lo mais complexo no entanto, usando credenciais diferentes, protocolos de autenticação alternativos e outros recursos de segurança.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Configurando um computador para uma conexão remota

Antes de poder acessar um sistema remoto com o WMI, talvez seja necessário verificar algumas configurações de segurança para confirmar se você tem acesso. Especificamente:

-   O Windows contém vários recursos de segurança que podem bloquear o acesso a scripts em sistemas remotos. Assim, talvez seja necessário modificar as configurações de Active Directory do seu sistema e do firewall do Windows antes de fazer uma chamada de WMI. Para obter mais informações, consulte [Configurando uma conexão WMI remota](connecting-to-wmi-remotely-starting-with-vista.md) e [Solucionando problemas de uma conexão WMI remota](troubleshooting-a-remote-wmi-connection.md).

-   As configurações corretas do DCOM devem ser habilitadas para que uma conexão remota funcione. Alterar as configurações do DCOM pode permitir que usuários com direitos limitados acessem um computador para uma conexão remota. Para obter mais informações, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).

Além disso, pode haver algumas circunstâncias em que você pode desejar executar o WMI por meio de uma porta fixa. Para fazer isso, também será necessário alterar as configurações. Para obter mais informações, consulte [Configurando uma porta fixa para o WMI](setting-up-a-fixed-port-for-wmi.md).

## <a name="connecting-to-a-remote-computer"></a>Conectando a um computador remoto

Em seu coração, conectar-se a um sistema remoto com o WMI consiste em verificar se você tem as permissões apropriadas para acessar o sistema e se sua conexão está configurada corretamente. Depois que você tiver esses dois elementos, a própria conexão será relativamente simples. Por exemplo, se você estiver usando suas credenciais de segurança padrão, poderá acessar o WMI em um sistema remoto usando o seguinte código:

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Conectando-se ao WMI remotamente com o PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Use o parâmetro *-ComputerName* comum para a maioria dos cmdlets do WMI, como [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Conectando-se ao WMI remotamente com o VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Use um moniker que contenha o nome do sistema remoto na chamada de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conectando-se ao WMI remotamente com C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Para a versão atual da interface gerenciada por WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use o objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) para representar uma conexão com um host remoto.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conectando-se ao WMI remotamente com C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Para a versão v1 da interface gerenciada por WMI ([System. Management](/dotnet/api/system.management)), use o objeto [ManagementScope](/dotnet/api/system.management.managementscope) para representar uma conexão com um host remoto.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Exemplo: obtendo dados WMI de um computador remoto (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Use o método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para especificar o nome do computador remoto no parâmetro *strNetworkResource* .


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

Os exemplos de código anteriores são, sem dúvida, a conexão remota mais básica que você pode executar com o WMI. Especificamente, os exemplos pressupõem o seguinte:

-   Você é um administrador no computador remoto. Devido ao [controle de conta de usuário](/previous-versions/aa905108(v=msdn.10)), a conta no sistema remoto deve ser uma conta de domínio no grupo Administradores. Para obter mais informações, consulte controle de conta de usuário e WMI.
-   A senha em seu computador local atual não está em branco. Isso é essencialmente um requisito de segurança do Windows que você deve ter feito logon em seu sistema com uma senha.
-   Os computadores locais e remotos estão dentro do mesmo domínio. Se você precisar cruzar os limites do domínio, precisará fornecer informações adicionais ou usar um modelo de programação ligeiramente diferente.
-   Você está usando sua própria conta para acessar o computador remoto. Se você estiver tentando acessar uma conta diferente, precisará fornecer credenciais adicionais. (Observe que a tentativa de acessar o WMI localmente com credenciais diferentes da sua conta atual não é permitida.)
-   Ambos os computadores estão executando o IPv6. O WMI dá suporte a conexões com computadores que executam o IPv6. No entanto, o computador local e o "computador \_ B" devem estar executando o IPv6. Qualquer um dos computadores pode estar executando o IPv4 também. Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md).
-   Seu script não precisa delegar, ou seja, não precisa acessar computadores remotos adicionais por meio do computador remoto de destino. Para obter mais informações, consulte [delegando com o WMI](connecting-to-a-3rd-computer-delegation.md).
-   Você está tentando fazer uma chamada específica, em vez de criar um processo remoto. Para obter mais informações, consulte [criando processos remotamente usando o WMI](creating-processes-remotely.md).

Com essas restrições em mente, uma chamada WMI remota é muito semelhante a uma chamada WMI local. a única diferença é que você deve especificar o nome do sistema remoto. No entanto, você pode optar por alterar muitos desses recursos: usando credenciais diferentes ou roteando sua chamada por um computador de terceiros ou acessando um domínio diferente.

 

 
