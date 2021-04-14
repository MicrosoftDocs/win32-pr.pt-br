---
description: Conectar-se a um namespace do WMI em um computador remoto pode exigir que você altere as configurações do firewall do Windows, UAC (controle de conta de usuário), DCOM ou Gerenciador de objetos do modelo CIM (CIMOm).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configurando uma conexão WMI remota
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505715"
---
# <a name="setting-up-a-remote-wmi-connection"></a><span data-ttu-id="999d4-103">Configurando uma conexão WMI remota</span><span class="sxs-lookup"><span data-stu-id="999d4-103">Setting up a Remote WMI Connection</span></span>

<span data-ttu-id="999d4-104">Conectar-se a um namespace do WMI em um computador remoto pode exigir que você altere as configurações do [Firewall do Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [UAC (controle de conta de usuário)](/previous-versions/aa905108(v=msdn.10)), DCOM ou gerenciador de objetos do modelo CIM (CIMOM).</span><span class="sxs-lookup"><span data-stu-id="999d4-104">Connecting to a WMI namespace on a remote computer may require that you change the settings for [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)), DCOM, or Common Information Model Object Manager (CIMOM).</span></span>

<span data-ttu-id="999d4-105">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="999d4-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="999d4-106">Configurações do firewall do Windows</span><span class="sxs-lookup"><span data-stu-id="999d4-106">Windows Firewall Settings</span></span>](#windows-firewall-settings)
-   [<span data-ttu-id="999d4-107">Configurações de controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="999d4-107">User Account Control Settings</span></span>](#user-account-control-settings)
-   [<span data-ttu-id="999d4-108">Configurações do DCOM</span><span class="sxs-lookup"><span data-stu-id="999d4-108">DCOM Settings</span></span>](#dcom-settings)
-   [<span data-ttu-id="999d4-109">Configurações de CIMOm</span><span class="sxs-lookup"><span data-stu-id="999d4-109">CIMOM Settings</span></span>](#cimom-settings)
-   [<span data-ttu-id="999d4-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="999d4-110">Related topics</span></span>](#related-topics)

## <a name="windows-firewall-settings"></a><span data-ttu-id="999d4-111">Configurações de Firewall do Windows</span><span class="sxs-lookup"><span data-stu-id="999d4-111">Windows Firewall Settings</span></span>

<span data-ttu-id="999d4-112">As configurações do WMI para as configurações do firewall do Windows habilitam apenas conexões WMI, em vez de outros aplicativos DCOM.</span><span class="sxs-lookup"><span data-stu-id="999d4-112">WMI settings for Windows Firewall settings enable only WMI connections, rather than other DCOM applications as well.</span></span>

<span data-ttu-id="999d4-113">Uma exceção deve ser definida no firewall para WMI no computador de destino remoto.</span><span class="sxs-lookup"><span data-stu-id="999d4-113">An exception must be set in the firewall for WMI on the remote target computer.</span></span> <span data-ttu-id="999d4-114">A exceção para o WMI permite que o WMI receba conexões remotas e retornos de chamada assíncronos para Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="999d4-114">The exception for WMI allows WMI to receive remote connections and asynchronous callbacks to Unsecapp.exe.</span></span> <span data-ttu-id="999d4-115">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="999d4-115">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="999d4-116">Se um aplicativo cliente criar seu próprio coletor, esse coletor deverá ser explicitamente adicionado às exceções de firewall para permitir que os retornos de chamada sejam bem-sucedidos.</span><span class="sxs-lookup"><span data-stu-id="999d4-116">If a client application creates its own sink, that sink must be explicitly added to the firewall exceptions to allow callbacks to succeed.</span></span>

<span data-ttu-id="999d4-117">A exceção para o WMI também funcionará se o WMI tiver sido iniciado com uma porta fixa, usando o comando **/standalonehost winmgmt** .</span><span class="sxs-lookup"><span data-stu-id="999d4-117">The exception for WMI also works if WMI has been started with a fixed port, using the **winmgmt /standalonehost** command.</span></span> <span data-ttu-id="999d4-118">Para obter mais informações, consulte [Configurando uma porta fixa para o WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="999d4-118">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="999d4-119">Você pode habilitar ou desabilitar o tráfego WMI por meio da interface do usuário do firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="999d4-119">You can enable or disable WMI traffic through the Windows Firewall UI.</span></span>

<span data-ttu-id="999d4-120">**Para habilitar ou desabilitar o tráfego WMI usando a interface do usuário do firewall**</span><span class="sxs-lookup"><span data-stu-id="999d4-120">**To enable or disable WMI traffic using firewall UI**</span></span>

1.  <span data-ttu-id="999d4-121">No **painel de controle**, clique em **segurança** e, em seguida, clique em Firewall do **Windows**.</span><span class="sxs-lookup"><span data-stu-id="999d4-121">In the **Control Panel**, click **Security** and then click **Windows Firewall**.</span></span>
2.  <span data-ttu-id="999d4-122">Clique em **alterar configurações** e, em seguida, clique na guia **exceções** .</span><span class="sxs-lookup"><span data-stu-id="999d4-122">Click **Change Settings** and then click the **Exceptions** tab.</span></span>
3.  <span data-ttu-id="999d4-123">Na janela exceções, marque a caixa de seleção **Instrumentação de gerenciamento do Windows (WMI)** para habilitar o tráfego WMI por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="999d4-123">In the Exceptions window, select the check box for **Windows Management Instrumentation (WMI)** to enable WMI traffic through the firewall.</span></span> <span data-ttu-id="999d4-124">Para desabilitar o tráfego WMI, desmarque a caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="999d4-124">To disable WMI traffic, clear the check box.</span></span>

<span data-ttu-id="999d4-125">Você pode habilitar ou desabilitar o tráfego WMI por meio do firewall no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="999d4-125">You can enable or disable WMI traffic through the firewall at the command prompt.</span></span>

<span data-ttu-id="999d4-126">**Para habilitar ou desabilitar o tráfego WMI no prompt de comando usando o grupo de regras do WMI**</span><span class="sxs-lookup"><span data-stu-id="999d4-126">**To enable or disable WMI traffic at command prompt using WMI rule group**</span></span>

-   <span data-ttu-id="999d4-127">Use os comandos a seguir em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="999d4-127">Use the following commands at a command prompt.</span></span> <span data-ttu-id="999d4-128">Digite o seguinte para habilitar o tráfego WMI por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="999d4-128">Type the following to enable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="999d4-129">**netsh advfirewall firewall set rule Group = "Instrumentação de gerenciamento do Windows (WMI)" novo Enable = Yes**</span><span class="sxs-lookup"><span data-stu-id="999d4-129">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**</span></span>

    <span data-ttu-id="999d4-130">Digite o comando a seguir para desabilitar o tráfego WMI por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="999d4-130">Type the following command to disable WMI traffic through the firewall.</span></span>

    <span data-ttu-id="999d4-131">**netsh advfirewall firewall set rule Group = "Instrumentação de gerenciamento do Windows (WMI)" novo Enable = no**</span><span class="sxs-lookup"><span data-stu-id="999d4-131">**netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**</span></span>

<span data-ttu-id="999d4-132">Em vez de usar o comando de grupo de regras de WMI único, você também pode usar comandos individuais para cada um dos serviços DCOM, WMI e coletor.</span><span class="sxs-lookup"><span data-stu-id="999d4-132">Rather than using the single WMI rule group command, you also can use individual commands for each of the DCOM, WMI service, and sink.</span></span>

<span data-ttu-id="999d4-133">**Para habilitar o tráfego WMI usando regras separadas para DCOM, WMI, coletor de retorno de chamada e conexões de saída**</span><span class="sxs-lookup"><span data-stu-id="999d4-133">**To enable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="999d4-134">Para estabelecer uma exceção de firewall para a porta DCOM 135, use o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="999d4-134">To establish a firewall exception for DCOM port 135, use the following command.</span></span>

    <span data-ttu-id="999d4-135">**netsh advfirewall firewall Adicionar regra dir = in name = "DCOM" Program =% raiz_do_sistema% \\ system32 \\svchost.exe Service = RPCSS Action = Allow Protocol = TCP localPort = 135**</span><span class="sxs-lookup"><span data-stu-id="999d4-135">**netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot%\\system32\\svchost.exe service=rpcss action=allow protocol=TCP localport=135**</span></span>

2.  <span data-ttu-id="999d4-136">Para estabelecer uma exceção de firewall para o serviço WMI, use o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="999d4-136">To establish a firewall exception for the WMI service, use the following command.</span></span>

    <span data-ttu-id="999d4-137">**netsh advfirewall firewall add rule dir = in name = "WMI" programa =% SystemRoot% \\ system32 \\svchost.exe Service = winmgmt Action = permitir protocolo = TCP localPort = any**</span><span class="sxs-lookup"><span data-stu-id="999d4-137">**netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot%\\system32\\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**</span></span>

3.  <span data-ttu-id="999d4-138">Para estabelecer uma exceção de firewall para o coletor que recebe retornos de chamada de um computador remoto, use o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="999d4-138">To establish a firewall exception for the sink that receives callbacks from a remote computer, use the following command.</span></span>

    <span data-ttu-id="999d4-139">**netsh advfirewall firewall add rule dir = in name = "UnsecApp" programa =% SystemRoot% \\ System32 \\ WBEM \\unsecapp.exe ação = permitir**</span><span class="sxs-lookup"><span data-stu-id="999d4-139">**netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot%\\system32\\wbem\\unsecapp.exe action=allow**</span></span>

4.  <span data-ttu-id="999d4-140">Para estabelecer uma exceção de firewall para conexões de saída com um computador remoto em que o computador local está se comunicando de forma assíncrona, use o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="999d4-140">To establish a firewall exception for outgoing connections to a remote computer that the local computer is communicating with asynchronously, use the following command.</span></span>

    <span data-ttu-id="999d4-141">**netsh advfirewall firewall add rule dir = out Name = "WMI \_ out" programa =% SystemRoot% \\ System32 \\svchost.exe Service = winmgmt Action = permitir protocolo = TCP localPort = any**</span><span class="sxs-lookup"><span data-stu-id="999d4-141">**netsh advfirewall firewall add rule dir=out name ="WMI\_OUT" program=%systemroot%\\system32\\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**</span></span>

<span data-ttu-id="999d4-142">Para desabilitar as exceções de firewall separadamente, use os comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="999d4-142">To disable the firewall exceptions separately, use the following commands.</span></span>

<span data-ttu-id="999d4-143">**Para desabilitar o tráfego WMI usando regras separadas para DCOM, WMI, coletor de retorno de chamada e conexões de saída**</span><span class="sxs-lookup"><span data-stu-id="999d4-143">**To disable WMI traffic using separate rules for DCOM, WMI, callback sink and outgoing connections**</span></span>

1.  <span data-ttu-id="999d4-144">Para desabilitar a exceção DCOM.</span><span class="sxs-lookup"><span data-stu-id="999d4-144">To disable the DCOM exception.</span></span>

    <span data-ttu-id="999d4-145">**netsh advfirewall firewall delete rule name = "DCOM"**</span><span class="sxs-lookup"><span data-stu-id="999d4-145">**netsh advfirewall firewall delete rule name="DCOM"**</span></span>

2.  <span data-ttu-id="999d4-146">Para desabilitar a exceção do serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="999d4-146">To disable the WMI service exception.</span></span>

    <span data-ttu-id="999d4-147">**netsh advfirewall firewall delete rule name = "WMI"**</span><span class="sxs-lookup"><span data-stu-id="999d4-147">**netsh advfirewall firewall delete rule name="WMI"**</span></span>

3.  <span data-ttu-id="999d4-148">Para desabilitar a exceção de coletor.</span><span class="sxs-lookup"><span data-stu-id="999d4-148">To disable the sink exception.</span></span>

    <span data-ttu-id="999d4-149">**netsh advfirewall firewall delete rule name = "UnsecApp"**</span><span class="sxs-lookup"><span data-stu-id="999d4-149">**netsh advfirewall firewall delete rule name="UnsecApp"**</span></span>

4.  <span data-ttu-id="999d4-150">Para desabilitar a exceção de saída.</span><span class="sxs-lookup"><span data-stu-id="999d4-150">To disable the outgoing exception.</span></span>

    <span data-ttu-id="999d4-151">**netsh advfirewall firewall delete rule name = "WMI \_ out"**</span><span class="sxs-lookup"><span data-stu-id="999d4-151">**netsh advfirewall firewall delete rule name="WMI\_OUT"**</span></span>

## <a name="user-account-control-settings"></a><span data-ttu-id="999d4-152">Configurações de controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="999d4-152">User Account Control Settings</span></span>

<span data-ttu-id="999d4-153">Acesso de controle de conta de usuário (UAC)-a filtragem de token pode afetar quais operações são permitidas em namespaces WMI ou quais dados são retornados.</span><span class="sxs-lookup"><span data-stu-id="999d4-153">User Account Control (UAC) access-token filtering can affect which operations are allowed in WMI namespaces or what data is returned.</span></span> <span data-ttu-id="999d4-154">No UAC, todas as contas no grupo Administradores local são executadas com um [*token de acesso*](/windows/desktop/SecGloss/a-gly)de usuário padrão, também conhecido como filtragem de token de acesso do UAC.</span><span class="sxs-lookup"><span data-stu-id="999d4-154">Under UAC, all accounts in the local Administrators group run with a standard user [*access token*](/windows/desktop/SecGloss/a-gly), also known as UAC access-token filtering.</span></span> <span data-ttu-id="999d4-155">Uma conta de administrador pode executar um script com um privilégio elevado: "executar como administrador".</span><span class="sxs-lookup"><span data-stu-id="999d4-155">An administrator account can run a script with an elevated privilege—"Run as Administrator".</span></span>

<span data-ttu-id="999d4-156">Quando você não estiver se conectando à conta de administrador interno, o UAC afetará as conexões com um computador remoto de forma diferente, dependendo se os dois computadores estão em um domínio ou em um grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="999d4-156">When you are not connecting to the built-in Administrator account, UAC affects connections to a remote computer differently depending on whether the two computers are in a domain or a workgroup.</span></span> <span data-ttu-id="999d4-157">Para obter mais informações sobre o UAC e conexões remotas, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="999d4-157">For more information about UAC and remote connections, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="dcom-settings"></a><span data-ttu-id="999d4-158">Configurações do DCOM</span><span class="sxs-lookup"><span data-stu-id="999d4-158">DCOM Settings</span></span>

<span data-ttu-id="999d4-159">Para obter mais informações sobre as configurações do DCOM, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="999d4-159">For more information on DCOM settings, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span> <span data-ttu-id="999d4-160">No entanto, o UAC afeta as conexões para contas de usuário que não são de domínio.</span><span class="sxs-lookup"><span data-stu-id="999d4-160">However, UAC affects connections for nondomain user accounts.</span></span> <span data-ttu-id="999d4-161">Se você se conectar a um computador remoto usando uma conta de usuário que não seja de domínio incluída no grupo local de administradores do computador remoto, você deverá conceder explicitamente acesso remoto DCOM, ativação e direitos de inicialização à conta.</span><span class="sxs-lookup"><span data-stu-id="999d4-161">If you connect to a remote computer using a nondomain user account included in the local Administrators group of the remote computer, then you must explicitly grant remote DCOM access, activation, and launch rights to the account.</span></span>

## <a name="cimom-settings"></a><span data-ttu-id="999d4-162">Configurações de CIMOm</span><span class="sxs-lookup"><span data-stu-id="999d4-162">CIMOM Settings</span></span>

<span data-ttu-id="999d4-163">As configurações de CIMOm devem ser atualizadas se a conexão remota estiver entre computadores que não têm uma relação de confiança; caso contrário, uma conexão assíncrona falhará.</span><span class="sxs-lookup"><span data-stu-id="999d4-163">The CIMOM settings need to be updated if the remote connection is between computers that do not have a trust relationship; otherwise, an asynchronous connection will fail.</span></span> <span data-ttu-id="999d4-164">Essa configuração não deve ser modificada para computadores no mesmo domínio ou em domínios confiáveis.</span><span class="sxs-lookup"><span data-stu-id="999d4-164">This setting should not be modified for computers in the same domain or in trusted domains.</span></span>

<span data-ttu-id="999d4-165">A seguinte entrada do registro precisa ser modificada para permitir retornos de chamada anônimos:</span><span class="sxs-lookup"><span data-stu-id="999d4-165">The following registry entry needs to be modified to allow anonymous callbacks:</span></span>

<span data-ttu-id="999d4-166">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**</span><span class="sxs-lookup"><span data-stu-id="999d4-166">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**AllowAnonymousCallback**</span></span><dl> <dt>

               Data type
</dt> <dd>               <span data-ttu-id="999d4-167">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="999d4-167">REG\_DWORD</span></span></dd> </dl>

<span data-ttu-id="999d4-168">Se o valor de **AllowAnonymousCallback** for definido como 0, o serviço WMI impedirá retornos de chamada anônimos para o cliente.</span><span class="sxs-lookup"><span data-stu-id="999d4-168">If the **AllowAnonymousCallback** value is set to 0, the WMI service prevents anonymous callbacks to the client.</span></span> <span data-ttu-id="999d4-169">Se o valor for definido como 1, o serviço WMI permitirá retornos de chamada anônimos para o cliente.</span><span class="sxs-lookup"><span data-stu-id="999d4-169">If the value is set to 1, the WMI service allows anonymous callbacks to the client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="999d4-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="999d4-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="999d4-171">Conectando-se ao WMI em um computador remoto</span><span class="sxs-lookup"><span data-stu-id="999d4-171">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
