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
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="68c6c-103">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="68c6c-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="68c6c-104">O WMI pode ser usado para gerenciar e acessar dados do WMI em computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="68c6c-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="68c6c-105">As conexões remotas no WMI são afetadas pelo [Firewall do Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) e pelas configurações do DCOM.</span><span class="sxs-lookup"><span data-stu-id="68c6c-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="68c6c-106">O [UAC (controle de conta de usuário)](/previous-versions/aa905108(v=msdn.10)) também pode exigir alterações em algumas configurações.</span><span class="sxs-lookup"><span data-stu-id="68c6c-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="68c6c-107">No entanto, depois que suas configurações estiverem corretas, a chamada para um sistema remoto será muito semelhante a uma chamada de WMI local.</span><span class="sxs-lookup"><span data-stu-id="68c6c-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="68c6c-108">Você pode optar por torná-lo mais complexo no entanto, usando credenciais diferentes, protocolos de autenticação alternativos e outros recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="68c6c-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="68c6c-109">Configurando um computador para uma conexão remota</span><span class="sxs-lookup"><span data-stu-id="68c6c-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="68c6c-110">Antes de poder acessar um sistema remoto com o WMI, talvez seja necessário verificar algumas configurações de segurança para confirmar se você tem acesso.</span><span class="sxs-lookup"><span data-stu-id="68c6c-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="68c6c-111">Especificamente:</span><span class="sxs-lookup"><span data-stu-id="68c6c-111">Specifically:</span></span>

-   <span data-ttu-id="68c6c-112">O Windows contém vários recursos de segurança que podem bloquear o acesso a scripts em sistemas remotos.</span><span class="sxs-lookup"><span data-stu-id="68c6c-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="68c6c-113">Assim, talvez seja necessário modificar as configurações de Active Directory do seu sistema e do firewall do Windows antes de fazer uma chamada de WMI.</span><span class="sxs-lookup"><span data-stu-id="68c6c-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="68c6c-114">Para obter mais informações, consulte [Configurando uma conexão WMI remota](connecting-to-wmi-remotely-starting-with-vista.md) e [Solucionando problemas de uma conexão WMI remota](troubleshooting-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68c6c-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="68c6c-115">As configurações corretas do DCOM devem ser habilitadas para que uma conexão remota funcione.</span><span class="sxs-lookup"><span data-stu-id="68c6c-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="68c6c-116">Alterar as configurações do DCOM pode permitir que usuários com direitos limitados acessem um computador para uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="68c6c-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="68c6c-117">Para obter mais informações, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68c6c-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="68c6c-118">Além disso, pode haver algumas circunstâncias em que você pode desejar executar o WMI por meio de uma porta fixa.</span><span class="sxs-lookup"><span data-stu-id="68c6c-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="68c6c-119">Para fazer isso, também será necessário alterar as configurações.</span><span class="sxs-lookup"><span data-stu-id="68c6c-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="68c6c-120">Para obter mais informações, consulte [Configurando uma porta fixa para o WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="68c6c-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="68c6c-121">Conectando a um computador remoto</span><span class="sxs-lookup"><span data-stu-id="68c6c-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="68c6c-122">Em seu coração, conectar-se a um sistema remoto com o WMI consiste em verificar se você tem as permissões apropriadas para acessar o sistema e se sua conexão está configurada corretamente.</span><span class="sxs-lookup"><span data-stu-id="68c6c-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="68c6c-123">Depois que você tiver esses dois elementos, a própria conexão será relativamente simples.</span><span class="sxs-lookup"><span data-stu-id="68c6c-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="68c6c-124">Por exemplo, se você estiver usando suas credenciais de segurança padrão, poderá acessar o WMI em um sistema remoto usando o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="68c6c-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="68c6c-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Conectando-se ao WMI remotamente com o PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="68c6c-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="68c6c-126">Use o parâmetro *-ComputerName* comum para a maioria dos cmdlets do WMI, como [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="68c6c-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="68c6c-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Conectando-se ao WMI remotamente com o VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="68c6c-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="68c6c-128">Use um moniker que contenha o nome do sistema remoto na chamada de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="68c6c-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="68c6c-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conectando-se ao WMI remotamente com C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="68c6c-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="68c6c-130">Para a versão atual da interface gerenciada por WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use o objeto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) para representar uma conexão com um host remoto.</span><span class="sxs-lookup"><span data-stu-id="68c6c-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="68c6c-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Conectando-se ao WMI remotamente com C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="68c6c-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="68c6c-132">Para a versão v1 da interface gerenciada por WMI ([System. Management](/dotnet/api/system.management)), use o objeto [ManagementScope](/dotnet/api/system.management.managementscope) para representar uma conexão com um host remoto.</span><span class="sxs-lookup"><span data-stu-id="68c6c-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="68c6c-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Exemplo: obtendo dados WMI de um computador remoto (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="68c6c-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="68c6c-134">Use o método [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para especificar o nome do computador remoto no parâmetro *strNetworkResource* .</span><span class="sxs-lookup"><span data-stu-id="68c6c-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


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

<span data-ttu-id="68c6c-135">Os exemplos de código anteriores são, sem dúvida, a conexão remota mais básica que você pode executar com o WMI.</span><span class="sxs-lookup"><span data-stu-id="68c6c-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="68c6c-136">Especificamente, os exemplos pressupõem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="68c6c-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="68c6c-137">Você é um administrador no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="68c6c-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="68c6c-138">Devido ao [controle de conta de usuário](/previous-versions/aa905108(v=msdn.10)), a conta no sistema remoto deve ser uma conta de domínio no grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="68c6c-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="68c6c-139">Para obter mais informações, consulte controle de conta de usuário e WMI.</span><span class="sxs-lookup"><span data-stu-id="68c6c-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="68c6c-140">A senha em seu computador local atual não está em branco.</span><span class="sxs-lookup"><span data-stu-id="68c6c-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="68c6c-141">Isso é essencialmente um requisito de segurança do Windows que você deve ter feito logon em seu sistema com uma senha.</span><span class="sxs-lookup"><span data-stu-id="68c6c-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="68c6c-142">Os computadores locais e remotos estão dentro do mesmo domínio.</span><span class="sxs-lookup"><span data-stu-id="68c6c-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="68c6c-143">Se você precisar cruzar os limites do domínio, precisará fornecer informações adicionais ou usar um modelo de programação ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="68c6c-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="68c6c-144">Você está usando sua própria conta para acessar o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="68c6c-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="68c6c-145">Se você estiver tentando acessar uma conta diferente, precisará fornecer credenciais adicionais.</span><span class="sxs-lookup"><span data-stu-id="68c6c-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="68c6c-146">(Observe que a tentativa de acessar o WMI localmente com credenciais diferentes da sua conta atual não é permitida.)</span><span class="sxs-lookup"><span data-stu-id="68c6c-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="68c6c-147">Ambos os computadores estão executando o IPv6.</span><span class="sxs-lookup"><span data-stu-id="68c6c-147">Both computers are running IPv6.</span></span> <span data-ttu-id="68c6c-148">O WMI dá suporte a conexões com computadores que executam o IPv6.</span><span class="sxs-lookup"><span data-stu-id="68c6c-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="68c6c-149">No entanto, o computador local e o "computador \_ B" devem estar executando o IPv6.</span><span class="sxs-lookup"><span data-stu-id="68c6c-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="68c6c-150">Qualquer um dos computadores pode estar executando o IPv4 também.</span><span class="sxs-lookup"><span data-stu-id="68c6c-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="68c6c-151">Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="68c6c-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="68c6c-152">Seu script não precisa delegar, ou seja, não precisa acessar computadores remotos adicionais por meio do computador remoto de destino.</span><span class="sxs-lookup"><span data-stu-id="68c6c-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="68c6c-153">Para obter mais informações, consulte [delegando com o WMI](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="68c6c-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="68c6c-154">Você está tentando fazer uma chamada específica, em vez de criar um processo remoto.</span><span class="sxs-lookup"><span data-stu-id="68c6c-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="68c6c-155">Para obter mais informações, consulte [criando processos remotamente usando o WMI](creating-processes-remotely.md).</span><span class="sxs-lookup"><span data-stu-id="68c6c-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="68c6c-156">Com essas restrições em mente, uma chamada WMI remota é muito semelhante a uma chamada WMI local. a única diferença é que você deve especificar o nome do sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="68c6c-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="68c6c-157">No entanto, você pode optar por alterar muitos desses recursos: usando credenciais diferentes ou roteando sua chamada por um computador de terceiros ou acessando um domínio diferente.</span><span class="sxs-lookup"><span data-stu-id="68c6c-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
