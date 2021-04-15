---
title: 'Instalação e configuração para Gerenciamento Remoto do Windows '
description: Para que os scripts do Gerenciamento Remoto do Windows (WinRM) sejam executados e para que a ferramenta de linha de comando do **WinRM** execute operações de dados, o gerenciamento remoto do Windows (WinRM) deve estar instalado e configurado.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: 4ebe4094984f237a3c8949392e3e9a6b47b8afe6
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2021
ms.locfileid: "104500121"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a><span data-ttu-id="940d4-103">Instalação e configuração para Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="940d4-103">Installation and configuration for Windows Remote Management</span></span>

<span data-ttu-id="940d4-104">Para que os scripts do Gerenciamento Remoto do Windows (WinRM) sejam executados e para que a ferramenta de linha de comando do **WinRM** execute operações de dados, o gerenciamento remoto do Windows (WinRM) deve estar instalado e configurado.</span><span class="sxs-lookup"><span data-stu-id="940d4-104">For Windows Remote Management (WinRM) scripts to run, and for the **Winrm** command-line tool to perform data operations, Windows Remote Management (WinRM) has to be both installed and configured.</span></span>

<span data-ttu-id="940d4-105">Esses elementos também dependem da configuração do WinRM.</span><span class="sxs-lookup"><span data-stu-id="940d4-105">These elements also depend on WinRM configuration.</span></span>

- <span data-ttu-id="940d4-106">A ferramenta de linha de comando do [shell remoto do Windows](./windows-remote-management-glossary.md#w) (**WinRS**).</span><span class="sxs-lookup"><span data-stu-id="940d4-106">The [Windows Remote Shell](./windows-remote-management-glossary.md#w) command-line tool (**Winrs**).</span></span>
- <span data-ttu-id="940d4-107">[Encaminhamento de eventos](./windows-remote-management-glossary.md#e).</span><span class="sxs-lookup"><span data-stu-id="940d4-107">[Event forwarding](./windows-remote-management-glossary.md#e).</span></span>
- <span data-ttu-id="940d4-108">Comunicação remota do Windows PowerShell 2,0.</span><span class="sxs-lookup"><span data-stu-id="940d4-108">Windows PowerShell 2.0 remoting.</span></span>

## <a name="where-winrm-is-installed"></a><span data-ttu-id="940d4-109">Onde o WinRM está instalado</span><span class="sxs-lookup"><span data-stu-id="940d4-109">Where WinRM is installed</span></span>

<span data-ttu-id="940d4-110">O WinRM é instalado automaticamente com todas as versões do sistema operacional Windows com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="940d4-110">WinRM is automatically installed with all currently-supported versions of the Windows operating system.</span></span>

## <a name="configuration-of-winrm-and-ipmi"></a><span data-ttu-id="940d4-111">Configuração do WinRM e do IPMI</span><span class="sxs-lookup"><span data-stu-id="940d4-111">Configuration of WinRM and IPMI</span></span>

<span data-ttu-id="940d4-112">Esses componentes do [provedor WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) do WinRM e do [IPMI (interface de gerenciamento de plataforma inteligente)](./windows-remote-management-glossary.md#i) são instalados com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="940d4-112">These WinRM and [Intelligent Platform Management Interface (IPMI)](./windows-remote-management-glossary.md#i) [WMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) components are installed with the operating system.</span></span>

- <span data-ttu-id="940d4-113">O serviço WinRM é iniciado automaticamente no Windows Server 2008 e em diante (no Windows Vista, você precisa iniciar o serviço manualmente).</span><span class="sxs-lookup"><span data-stu-id="940d4-113">The WinRM service starts automatically on Windows Server 2008 and on wards (on Windows Vista, you need to start the service manually).</span></span>
- <span data-ttu-id="940d4-114">Por padrão, nenhum [ouvinte](./windows-remote-management-glossary.md#l) do WinRM está configurado.</span><span class="sxs-lookup"><span data-stu-id="940d4-114">By default, no WinRM [listener](./windows-remote-management-glossary.md#l) is configured.</span></span> <span data-ttu-id="940d4-115">Mesmo que o serviço WinRM esteja em execução, WS-Management [mensagens](./windows-remote-management-glossary.md#m) de protocolo que solicitam dados não podem ser recebidas nem enviadas.</span><span class="sxs-lookup"><span data-stu-id="940d4-115">Even if the WinRM service is running, WS-Management protocol [messages](./windows-remote-management-glossary.md#m) that request data can't be received nor sent.</span></span>
- <span data-ttu-id="940d4-116">O firewall de conexão com a Internet (ICF) bloqueia o acesso às portas.</span><span class="sxs-lookup"><span data-stu-id="940d4-116">Internet Connection Firewall (ICF) blocks access to ports.</span></span>

<span data-ttu-id="940d4-117">Use o comando **WinRM** para localizar ouvintes e endereços digitando o comando a seguir em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="940d4-117">Use the **Winrm** command to locate listeners and the addresses by typing the following command at a command prompt.</span></span>

```console
winrm e winrm/config/listener
```

<span data-ttu-id="940d4-118">Para verificar o estado dos parâmetros de configuração, digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="940d4-118">To check the state of configuration settings, type the following command.</span></span>

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a><span data-ttu-id="940d4-119">Configuração padrão rápida</span><span class="sxs-lookup"><span data-stu-id="940d4-119">Quick default configuration</span></span>

<span data-ttu-id="940d4-120">Você pode habilitar o protocolo WS-Management no computador local e definir a configuração padrão para gerenciamento remoto com o comando `winrm quickconfig` .</span><span class="sxs-lookup"><span data-stu-id="940d4-120">You can enable the WS-Management protocol on the local computer, and set up the default configuration for remote management with the command `winrm quickconfig`.</span></span>

<span data-ttu-id="940d4-121">O `winrm quickconfig` comando (ou a versão abreviada `winrm qc` ) executa essas operações.</span><span class="sxs-lookup"><span data-stu-id="940d4-121">The `winrm quickconfig` command (or the abbreviated version `winrm qc`) performs these operations.</span></span>

- <span data-ttu-id="940d4-122">Inicia o serviço WinRM e define o tipo de inicialização do serviço como iniciar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="940d4-122">Starts the WinRM service, and sets the service startup type to auto-start.</span></span>
- <span data-ttu-id="940d4-123">Configura um ouvinte para as portas que enviam e recebem WS-Management [mensagens](./windows-remote-management-glossary.md#m) de protocolo usando http ou HTTPS em qualquer endereço IP.</span><span class="sxs-lookup"><span data-stu-id="940d4-123">Configures a listener for the ports that send and receive WS-Management protocol [messages](./windows-remote-management-glossary.md#m) using either HTTP or HTTPS on any IP address.</span></span>
- <span data-ttu-id="940d4-124">Define as exceções do ICF para o serviço WinRM e abre as portas para HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="940d4-124">Defines ICF exceptions for the WinRM service, and opens the ports for HTTP and HTTPS.</span></span>

> [!NOTE]
> <span data-ttu-id="940d4-125">O `winrm quickconfig` comando cria uma exceção de firewall somente para o perfil de usuário atual.</span><span class="sxs-lookup"><span data-stu-id="940d4-125">The `winrm quickconfig` command creates a firewall exception only for the current user profile.</span></span> <span data-ttu-id="940d4-126">Se o perfil de firewall for alterado por qualquer motivo, você deverá executar `winrm quickconfig` o para habilitar a exceção de firewall para o novo perfil; caso contrário, a exceção poderá não estar habilitada.</span><span class="sxs-lookup"><span data-stu-id="940d4-126">If the firewall profile is changed for any reason, you should run `winrm quickconfig` to enable the firewall exception for the new profile; otherwise, the exception might not be enabled.</span></span>

<span data-ttu-id="940d4-127">Para recuperar informações sobre como personalizar uma configuração, digite `winrm help config` em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="940d4-127">To retrieve information about customizing a configuration, type `winrm help config` at a command prompt.</span></span>

### <a name="to-configure-winrm-with-default-settings"></a><span data-ttu-id="940d4-128">Para configurar o WinRM com as configurações padrão</span><span class="sxs-lookup"><span data-stu-id="940d4-128">To configure WinRM with default settings</span></span>

1. <span data-ttu-id="940d4-129">Digite `winrm quickconfig` em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="940d4-129">Type `winrm quickconfig` at a command prompt.</span></span>

   <span data-ttu-id="940d4-130">Se você não estiver executando sob a conta de administrador do computador local, deverá selecionar **Executar como administrador** no menu **Iniciar** ou usar o comando **runas** em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="940d4-130">If you're not running under the local computer Administrator account, then you must either select **Run as Administrator** from the **Start** menu, or use the **Runas** command at a command prompt.</span></span>

2. <span data-ttu-id="940d4-131">Quando a ferramenta exibe **fazer essas alterações \[ y/n \] ?**, digite **y**.</span><span class="sxs-lookup"><span data-stu-id="940d4-131">When the tool displays **Make these changes \[y/n\]?**, type **y**.</span></span>

   <span data-ttu-id="940d4-132">Se a configuração for bem-sucedida, a saída a seguir será exibida.</span><span class="sxs-lookup"><span data-stu-id="940d4-132">If configuration is successful, then the following output is displayed.</span></span>

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. <span data-ttu-id="940d4-133">Mantenha as configurações padrão dos componentes cliente e servidor do WinRM ou personalize-os.</span><span class="sxs-lookup"><span data-stu-id="940d4-133">Keep the default settings for client and server components of WinRM, or customize them.</span></span> <span data-ttu-id="940d4-134">Por exemplo, talvez seja necessário adicionar determinados computadores remotos à lista TrustedHosts de configuração do cliente.</span><span class="sxs-lookup"><span data-stu-id="940d4-134">For example, you might need to add certain remote computers to the client configuration TrustedHosts list.</span></span>

   <span data-ttu-id="940d4-135">Você deve configurar uma lista de hosts confiáveis quando a autenticação mútua não puder ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="940d4-135">You should set up a trusted hosts list when mutual authentication can't be established.</span></span> <span data-ttu-id="940d4-136">O Kerberos permite a autenticação mútua, mas não pode ser usado somente em domínios de grupos de &mdash; domínio.</span><span class="sxs-lookup"><span data-stu-id="940d4-136">Kerberos allows mutual authentication, but it can't be used in workgroups&mdash;only domains.</span></span> <span data-ttu-id="940d4-137">Uma prática recomendada ao configurar hosts confiáveis para um grupo de trabalho é tornar a lista o mais restrito possível.</span><span class="sxs-lookup"><span data-stu-id="940d4-137">A best practice when setting up trusted hosts for a workgroup is to make the list as restricted as possible.</span></span>

4. <span data-ttu-id="940d4-138">Crie um ouvinte HTTPS digitando o comando `winrm quickconfig -transport:https` .</span><span class="sxs-lookup"><span data-stu-id="940d4-138">Create an HTTPS listener by typing the command `winrm quickconfig -transport:https`.</span></span> <span data-ttu-id="940d4-139">Lembre-se de que você deve abrir a porta 5986 para que o transporte HTTPS funcione.</span><span class="sxs-lookup"><span data-stu-id="940d4-139">Be aware that you must open port 5986 for HTTPS transport to work.</span></span>

## <a name="listener-and-ws-management-protocol-default-settings"></a><span data-ttu-id="940d4-140">Configurações padrão do protocolo ouvinte e WS-Management</span><span class="sxs-lookup"><span data-stu-id="940d4-140">Listener and WS-Management protocol default settings</span></span>

<span data-ttu-id="940d4-141">Para obter a configuração do ouvinte, digite `winrm enumerate winrm/config/listener` em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="940d4-141">To get the listener configuration, type `winrm enumerate winrm/config/listener` at a command prompt.</span></span> <span data-ttu-id="940d4-142">Os ouvintes são definidos por um transporte (HTTP ou HTTPS) e um endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="940d4-142">Listeners are defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span>

<span data-ttu-id="940d4-143">`winrm quickconfig` cria as seguintes configurações padrão para um ouvinte.</span><span class="sxs-lookup"><span data-stu-id="940d4-143">`winrm quickconfig` creates the following default settings for a listener.</span></span> <span data-ttu-id="940d4-144">Você pode criar mais de um ouvinte.</span><span class="sxs-lookup"><span data-stu-id="940d4-144">You can create more than one listener.</span></span> <span data-ttu-id="940d4-145">Para obter mais informações, digite `winrm help config` em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="940d4-145">For more information, type `winrm help config` at a command prompt.</span></span>

### <a name="address"></a><span data-ttu-id="940d4-146">Endereço</span><span class="sxs-lookup"><span data-stu-id="940d4-146">Address</span></span>

<span data-ttu-id="940d4-147">Especifica o endereço para o qual este ouvinte foi criado.</span><span class="sxs-lookup"><span data-stu-id="940d4-147">Specifies the address for which this listener was created.</span></span>

### <a name="transport"></a><span data-ttu-id="940d4-148">Transport</span><span class="sxs-lookup"><span data-stu-id="940d4-148">Transport</span></span>

<span data-ttu-id="940d4-149">Especifica o transporte a ser usado para enviar e receber respostas e solicitações do protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="940d4-149">Specifies the transport to use to send and receive WS-Management protocol requests and responses.</span></span> <span data-ttu-id="940d4-150">O valor deve ser *http* ou *https*.</span><span class="sxs-lookup"><span data-stu-id="940d4-150">The value must be either *HTTP* or *HTTPS*.</span></span> <span data-ttu-id="940d4-151">O padrão é *http*.</span><span class="sxs-lookup"><span data-stu-id="940d4-151">The default is *HTTP*.</span></span>

### <a name="port"></a><span data-ttu-id="940d4-152">Porta</span><span class="sxs-lookup"><span data-stu-id="940d4-152">Port</span></span>

<span data-ttu-id="940d4-153">Especifica a porta TCP para a qual este ouvinte é criado.</span><span class="sxs-lookup"><span data-stu-id="940d4-153">Specifies the TCP port for which this listener is created.</span></span>

<span data-ttu-id="940d4-154">**WinRM 2,0:** A porta HTTP padrão é 5985.</span><span class="sxs-lookup"><span data-stu-id="940d4-154">**WinRM 2.0:** The default HTTP port is 5985.</span></span>

### <a name="hostname"></a><span data-ttu-id="940d4-155">Nome do host</span><span class="sxs-lookup"><span data-stu-id="940d4-155">Hostname</span></span>

<span data-ttu-id="940d4-156">Especifica o nome do host do computador no qual o serviço WinRM está em execução.</span><span class="sxs-lookup"><span data-stu-id="940d4-156">Specifies the host name of the computer on which the WinRM service is running.</span></span> <span data-ttu-id="940d4-157">O valor deve ser um nome de domínio totalmente qualificado ou uma cadeia de caracteres literal IPv4 ou IPv6, ou um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="940d4-157">The value must be a fully-qualified domain name, or an IPv4 or IPv6 literal string, or a wildcard character.</span></span>

### <a name="enabled"></a><span data-ttu-id="940d4-158">habilitado</span><span class="sxs-lookup"><span data-stu-id="940d4-158">Enabled</span></span>

<span data-ttu-id="940d4-159">Especifica se o ouvinte está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="940d4-159">Specifies whether the listener is enabled or disabled.</span></span> <span data-ttu-id="940d4-160">O valor padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-160">The default value is *True*.</span></span>

### <a name="urlprefix"></a><span data-ttu-id="940d4-161">URLPrefix</span><span class="sxs-lookup"><span data-stu-id="940d4-161">URLPrefix</span></span>

<span data-ttu-id="940d4-162">Especifica um prefixo de URL no qual aceitar solicitações HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="940d4-162">Specifies a URL prefix on which to accept HTTP or HTTPS requests.</span></span> <span data-ttu-id="940d4-163">Esta é uma cadeia de caracteres que contém apenas os caracteres de a-z, A-Z, 9-0, sublinhado ( \_ ) e barra (/).</span><span class="sxs-lookup"><span data-stu-id="940d4-163">This is a string containing only the characters a-z, A-Z, 9-0, underscore (\_), and slash (/).</span></span> <span data-ttu-id="940d4-164">A cadeia de caracteres não deve começar com ou terminar com uma barra (/).</span><span class="sxs-lookup"><span data-stu-id="940d4-164">The string must not start with or end with a slash (/).</span></span> <span data-ttu-id="940d4-165">Por exemplo, se o nome do computador for SampleMachine, o cliente WinRM especificará https://SampleMachine/< *URLPrefix*> no endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="940d4-165">For example, if the computer name is SampleMachine, then the WinRM client would specify https://SampleMachine/<*URLPrefix*> in the destination address.</span></span> <span data-ttu-id="940d4-166">O prefixo de URL padrão é "WSMan".</span><span class="sxs-lookup"><span data-stu-id="940d4-166">The default URL prefix is "wsman".</span></span>

### <a name="certificatethumbprint"></a><span data-ttu-id="940d4-167">CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="940d4-167">CertificateThumbprint</span></span>

<span data-ttu-id="940d4-168">Especifica a impressão digital do certificado de serviço.</span><span class="sxs-lookup"><span data-stu-id="940d4-168">Specifies the thumbprint of the service certificate.</span></span> <span data-ttu-id="940d4-169">Esse valor representa uma cadeia de caracteres de valores hexadecimais de dois dígitos encontrada no campo impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="940d4-169">This value represents a string of two-digit hexadecimal values found in the Thumbprint field of the certificate.</span></span> <span data-ttu-id="940d4-170">Essa cadeia de caracteres contém o hash SHA-1 do certificado.</span><span class="sxs-lookup"><span data-stu-id="940d4-170">This string contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="940d4-171">Os certificados são utilizados na autenticação baseada em certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="940d4-171">Certificates are used in client certificate-based authentication.</span></span> <span data-ttu-id="940d4-172">Os certificados podem ser mapeados somente para contas de usuário locais e não funcionam com contas de domínio.</span><span class="sxs-lookup"><span data-stu-id="940d4-172">Certificates can be mapped only to local user accounts, and they do not work with domain accounts.</span></span>

### <a name="listeningon"></a><span data-ttu-id="940d4-173">ListeningOn</span><span class="sxs-lookup"><span data-stu-id="940d4-173">ListeningOn</span></span>

<span data-ttu-id="940d4-174">Especifica os endereços IPv4 e IPv6 que o ouvinte usa.</span><span class="sxs-lookup"><span data-stu-id="940d4-174">Specifies the IPv4 and IPv6 addresses that the listener uses.</span></span> <span data-ttu-id="940d4-175">Por exemplo: "111.0.0.1, 111.222.333.444,:: 1, 1000:2000:2C: 3: c19:9ec8: a715:5e24, 3FFE: 8311: ffff: f70f: 0:5efe: 111.222.333.444, FE80:: 5efe: 111.222.333.444% 8, FE80:: c19:9ec8: a715:5e24% 6".</span><span class="sxs-lookup"><span data-stu-id="940d4-175">For example: "111.0.0.1, 111.222.333.444, ::1, 1000:2000:2c:3:c19:9ec8:a715:5e24, 3ffe:8311:ffff:f70f:0:5efe:111.222.333.444, fe80::5efe:111.222.333.444%8, fe80::c19:9ec8:a715:5e24%6".</span></span>

## <a name="protocol-default-settings"></a><span data-ttu-id="940d4-176">Configurações padrão de protocolo</span><span class="sxs-lookup"><span data-stu-id="940d4-176">Protocol default settings</span></span>

<span data-ttu-id="940d4-177">Muitas das definições de configuração, como MaxEnvelopeSizekb ou SoapTraceEnabled, determinam como os componentes do cliente e do servidor WinRM interagem com o protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="940d4-177">Many of the configuration settings, such as MaxEnvelopeSizekb or SoapTraceEnabled, determine how the WinRM client and server components interact with the WS-Management protocol.</span></span> <span data-ttu-id="940d4-178">A lista a seguir descreve as definições de configuração disponíveis.</span><span class="sxs-lookup"><span data-stu-id="940d4-178">The following list describes the available configuration settings.</span></span>

### <a name="maxenvelopesizekb"></a><span data-ttu-id="940d4-179">MaxEnvelopeSizekb</span><span class="sxs-lookup"><span data-stu-id="940d4-179">MaxEnvelopeSizekb</span></span>

<span data-ttu-id="940d4-180">Especifica os dados do protocolo SOAP (Simple Object Access Protocol) em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="940d4-180">Specifies the maximum Simple Object Access Protocol (SOAP) data in kilobytes.</span></span> <span data-ttu-id="940d4-181">O padrão é 150 quilobytes.</span><span class="sxs-lookup"><span data-stu-id="940d4-181">The default is 150 kilobytes.</span></span>

> [!NOTE]  
> <span data-ttu-id="940d4-182">O comportamento não será suportado se MaxEnvelopeSizekb for definido como um valor maior que 1039440.</span><span class="sxs-lookup"><span data-stu-id="940d4-182">The behavior is unsupported if MaxEnvelopeSizekb is set to a value greater than 1039440.</span></span>

### <a name="maxtimeoutms"></a><span data-ttu-id="940d4-183">MaxTimeoutms</span><span class="sxs-lookup"><span data-stu-id="940d4-183">MaxTimeoutms</span></span>

<span data-ttu-id="940d4-184">Especifica o tempo limite máximo, em milissegundos, que pode ser usado para qualquer solicitação que não sejam solicitações de pull.</span><span class="sxs-lookup"><span data-stu-id="940d4-184">Specifies the maximum time-out, in milliseconds, that can be used for any request other than Pull requests.</span></span> <span data-ttu-id="940d4-185">O padrão é 60000.</span><span class="sxs-lookup"><span data-stu-id="940d4-185">The default is 60000.</span></span>

### <a name="maxbatchitems"></a><span data-ttu-id="940d4-186">MaxBatchItems</span><span class="sxs-lookup"><span data-stu-id="940d4-186">MaxBatchItems</span></span>

<span data-ttu-id="940d4-187">Especifica o número máximo de elementos que podem ser usados em uma resposta de recepção.</span><span class="sxs-lookup"><span data-stu-id="940d4-187">Specifies the maximum number of elements that can be used in a Pull response.</span></span> <span data-ttu-id="940d4-188">O padrão é 32000.</span><span class="sxs-lookup"><span data-stu-id="940d4-188">The default is 32000.</span></span>

### <a name="maxproviderrequests"></a><span data-ttu-id="940d4-189">MaxProviderRequests</span><span class="sxs-lookup"><span data-stu-id="940d4-189">MaxProviderRequests</span></span>

<span data-ttu-id="940d4-190">Especifica o número máximo de solicitações simultâneas permitido pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="940d4-190">Specifies the maximum number of concurrent requests that are allowed by the service.</span></span> <span data-ttu-id="940d4-191">O padrão é 25.</span><span class="sxs-lookup"><span data-stu-id="940d4-191">The default is 25.</span></span>

<span data-ttu-id="940d4-192">**WinRM 2,0:** Essa configuração é preterida e é definida como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="940d4-192">**WinRM 2.0:** This setting is deprecated, and is set to read-only.</span></span>

## <a name="winrm-client-default-configuration-settings"></a><span data-ttu-id="940d4-193">Definições de configuração padrão do cliente WinRM</span><span class="sxs-lookup"><span data-stu-id="940d4-193">WinRM client default configuration settings</span></span>

<span data-ttu-id="940d4-194">A versão do cliente do WinRM tem as seguintes definições de configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="940d4-194">The client version of WinRM has the following default configuration settings.</span></span>

### <a name="networkdelayms"></a><span data-ttu-id="940d4-195">NetworkDelayms</span><span class="sxs-lookup"><span data-stu-id="940d4-195">NetworkDelayms</span></span>

<span data-ttu-id="940d4-196">Especifica o tempo extra, em milissegundos, que o computador cliente aguarda para acomodar o tempo de atraso de rede.</span><span class="sxs-lookup"><span data-stu-id="940d4-196">Specifies the extra time in milliseconds that the client computer waits to accommodate for network delay time.</span></span> <span data-ttu-id="940d4-197">O padrão é 5000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="940d4-197">The default is 5000 milliseconds.</span></span>

### <a name="urlprefix"></a><span data-ttu-id="940d4-198">URLPrefix</span><span class="sxs-lookup"><span data-stu-id="940d4-198">URLPrefix</span></span>

<span data-ttu-id="940d4-199">Especifica um prefixo de URL no qual aceitar solicitações HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="940d4-199">Specifies a URL prefix on which to accept HTTP or HTTPS requests.</span></span> <span data-ttu-id="940d4-200">O prefixo de URL padrão é "WSMan".</span><span class="sxs-lookup"><span data-stu-id="940d4-200">The default URL prefix is "wsman".</span></span>

### <a name="allowunencrypted"></a><span data-ttu-id="940d4-201">AllowUnencrypted</span><span class="sxs-lookup"><span data-stu-id="940d4-201">AllowUnencrypted</span></span>

<span data-ttu-id="940d4-202">Permite que o computador cliente solicite tráfego não criptografado.</span><span class="sxs-lookup"><span data-stu-id="940d4-202">Allows the client computer to request unencrypted traffic.</span></span> <span data-ttu-id="940d4-203">Por padrão, o computador cliente requer o tráfego de rede criptografado e essa configuração é *falsa*.</span><span class="sxs-lookup"><span data-stu-id="940d4-203">By default, the client computer requires encrypted network traffic and this setting is *False*.</span></span>

### <a name="basic"></a><span data-ttu-id="940d4-204">Básico</span><span class="sxs-lookup"><span data-stu-id="940d4-204">Basic</span></span>

<span data-ttu-id="940d4-205">Permite que o computador cliente use a autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="940d4-205">Allows the client computer to use Basic authentication.</span></span> <span data-ttu-id="940d4-206">A autenticação básica é um esquema no qual o nome de usuário e a senha são enviados em texto não criptografado para o servidor ou proxy.</span><span class="sxs-lookup"><span data-stu-id="940d4-206">Basic authentication is a scheme in which the user name and password are sent in clear text to the server or proxy.</span></span> <span data-ttu-id="940d4-207">Esse método é o método menos seguro de autenticação.</span><span class="sxs-lookup"><span data-stu-id="940d4-207">This method is the least secure method of authentication.</span></span> <span data-ttu-id="940d4-208">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-208">The default is *True*.</span></span>

### <a name="digest"></a><span data-ttu-id="940d4-209">Digest</span><span class="sxs-lookup"><span data-stu-id="940d4-209">Digest</span></span>

<span data-ttu-id="940d4-210">Permite que o cliente use a autenticação Digest.</span><span class="sxs-lookup"><span data-stu-id="940d4-210">Allows the client to use Digest authentication.</span></span> <span data-ttu-id="940d4-211">É um esquema de desafio/resposta de autenticação que utiliza uma cadeia de caracteres de dados do servidor especificado para o desafio.</span><span class="sxs-lookup"><span data-stu-id="940d4-211">Digest authentication is a challenge-response scheme that uses a server-specified data string for the challenge.</span></span> <span data-ttu-id="940d4-212">Apenas o computador cliente pode iniciar uma solicitação de autenticação Digest.</span><span class="sxs-lookup"><span data-stu-id="940d4-212">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="940d4-213">O computador cliente envia uma solicitação ao servidor para autenticar e recebe uma cadeia de caracteres do token do servidor.</span><span class="sxs-lookup"><span data-stu-id="940d4-213">The client computer sends a request to the server to authenticate, and receives a token string from the server.</span></span> <span data-ttu-id="940d4-214">Em seguida, o computador cliente envia a solicitação de recurso, incluindo o nome de usuário e um hash criptográfico da senha combinada com a cadeia de caracteres do token.</span><span class="sxs-lookup"><span data-stu-id="940d4-214">Then the client computer sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="940d4-215">A autenticação Digest tem suporte para HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="940d4-215">Digest authentication is supported for HTTP and for HTTPS.</span></span> <span data-ttu-id="940d4-216">Os aplicativos e scripts de cliente do shell do WinRM podem especificar a autenticação Digest, mas o serviço WinRM não aceita a autenticação Digest.</span><span class="sxs-lookup"><span data-stu-id="940d4-216">WinRM Shell client scripts and applications can specify Digest authentication, but the WinRM service does not accept Digest authentication.</span></span> <span data-ttu-id="940d4-217">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-217">The default is *True*.</span></span>

> [!NOTE]
> <span data-ttu-id="940d4-218">A autenticação Digest por HTTP não é considerada segura.</span><span class="sxs-lookup"><span data-stu-id="940d4-218">Digest authentication over HTTP is not considered secure.</span></span>

### <a name="certificate"></a><span data-ttu-id="940d4-219">Certificado</span><span class="sxs-lookup"><span data-stu-id="940d4-219">Certificate</span></span>

<span data-ttu-id="940d4-220">Permite que o cliente use a autenticação baseada em certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="940d4-220">Allows the client to use client certificate-based authentication.</span></span> <span data-ttu-id="940d4-221">A autenticação baseada em certificado é um esquema no qual o servidor autentica um cliente identificado por um certificado X509.</span><span class="sxs-lookup"><span data-stu-id="940d4-221">Certificate-based authentication is a scheme in which the server authenticates a client identified by an X509 certificate.</span></span> <span data-ttu-id="940d4-222">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-222">The default is *True*.</span></span>

### <a name="kerberos"></a><span data-ttu-id="940d4-223">Kerberos</span><span class="sxs-lookup"><span data-stu-id="940d4-223">Kerberos</span></span>

<span data-ttu-id="940d4-224">Permite que o cliente use a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="940d4-224">Allows the client to use Kerberos authentication.</span></span> <span data-ttu-id="940d4-225">A autenticação Kerberos é um esquema no qual o cliente e o servidor autenticam mutuamente usando certificados Kerberos.</span><span class="sxs-lookup"><span data-stu-id="940d4-225">Kerberos authentication is a scheme in which the client and server mutually authenticate by using Kerberos certificates.</span></span> <span data-ttu-id="940d4-226">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-226">The default is *True*.</span></span>

### <a name="negotiate"></a><span data-ttu-id="940d4-227">Negotiate</span><span class="sxs-lookup"><span data-stu-id="940d4-227">Negotiate</span></span>

<span data-ttu-id="940d4-228">Permite que o cliente use a autenticação Negotiate.</span><span class="sxs-lookup"><span data-stu-id="940d4-228">Allows the client to use Negotiate authentication.</span></span> <span data-ttu-id="940d4-229">Negociar a autenticação é um esquema no qual o cliente envia uma solicitação ao servidor para autenticar.</span><span class="sxs-lookup"><span data-stu-id="940d4-229">Negotiate authentication is a scheme in which the client sends a request to the server to authenticate.</span></span> <span data-ttu-id="940d4-230">O servidor determina se deve usar o protocolo Kerberos ou NTLM.</span><span class="sxs-lookup"><span data-stu-id="940d4-230">The server determines whether to use the Kerberos protocol or NTLM.</span></span> <span data-ttu-id="940d4-231">O protocolo Kerberos é selecionado para autenticar uma conta de domínio e NTLM é selecionado para contas de computador local.</span><span class="sxs-lookup"><span data-stu-id="940d4-231">The Kerberos protocol is selected to authenticate a domain account, and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="940d4-232">O nome de usuário deve ser especificado no \\ \_ formato de nome de usuário de domínio para um usuário de domínio.</span><span class="sxs-lookup"><span data-stu-id="940d4-232">The user name must be specified in domain\\user\_name format for a domain user.</span></span> <span data-ttu-id="940d4-233">O nome de usuário deve ser especificado no \_ formato " \\ nome de usuário do nome do servidor \_ " para um usuário local em um computador servidor.</span><span class="sxs-lookup"><span data-stu-id="940d4-233">The user name must be specified in "server\_name\\user\_name" format for a local user on a server computer.</span></span> <span data-ttu-id="940d4-234">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-234">The default is *True*.</span></span>

### <a name="credssp"></a><span data-ttu-id="940d4-235">CredSSP</span><span class="sxs-lookup"><span data-stu-id="940d4-235">CredSSP</span></span>

<span data-ttu-id="940d4-236">Permite que o cliente use a autenticação do Credential Security Support Provider (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="940d4-236">Allows the client to use Credential Security Support Provider (CredSSP) authentication.</span></span> <span data-ttu-id="940d4-237">O CredSSP permite que um aplicativo delegue as credenciais do usuário do computador cliente para o servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="940d4-237">CredSSP enables an application to delegate the user's credentials from the client computer to the target server.</span></span> <span data-ttu-id="940d4-238">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-238">The default is *False*.</span></span>

### <a name="defaultports"></a><span data-ttu-id="940d4-239">DefaultPorts</span><span class="sxs-lookup"><span data-stu-id="940d4-239">DefaultPorts</span></span>

<span data-ttu-id="940d4-240">Especifica as portas que o cliente usará para HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="940d4-240">Specifies the ports that the client will use for either HTTP or HTTPS.</span></span>

<span data-ttu-id="940d4-241">**WinRM 2,0:** A porta HTTP padrão é 5985 e a porta HTTPS padrão é 5986.</span><span class="sxs-lookup"><span data-stu-id="940d4-241">**WinRM 2.0:** The default HTTP port is 5985, and the default HTTPS port is 5986.</span></span>

### <a name="trustedhosts"></a><span data-ttu-id="940d4-242">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="940d4-242">TrustedHosts</span></span>

<span data-ttu-id="940d4-243">Especifica a lista de computadores remotos que são confiáveis.</span><span class="sxs-lookup"><span data-stu-id="940d4-243">Specifies the list of remote computers that are trusted.</span></span> <span data-ttu-id="940d4-244">Outros computadores em um grupo de trabalho ou computadores em um domínio diferente devem ser adicionados a essa lista.</span><span class="sxs-lookup"><span data-stu-id="940d4-244">Other computers in a workgroup or computers in a different domain should be added to this list.</span></span>

> [!Note]
> <span data-ttu-id="940d4-245">Os computadores na lista TrustedHosts não são autenticados.</span><span class="sxs-lookup"><span data-stu-id="940d4-245">The computers in the TrustedHosts list are not authenticated.</span></span> <span data-ttu-id="940d4-246">O cliente pode enviar informações de credenciais para esses computadores.</span><span class="sxs-lookup"><span data-stu-id="940d4-246">The client may send credential information to these computers.</span></span>

<span data-ttu-id="940d4-247">Se um endereço IPv6 for especificado para um TrustedHost, o endereço deverá ser colocado entre colchetes, conforme demonstrado pelo seguinte comando do utilitário WinRM: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .</span><span class="sxs-lookup"><span data-stu-id="940d4-247">If an IPv6 address is specified for a TrustedHost, the address must be enclosed in square brackets as demonstrated by the following winrm utility command: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'`.</span></span>

<span data-ttu-id="940d4-248">Para obter mais informações sobre como adicionar computadores à lista TrustedHosts, digite `winrm help config` .</span><span class="sxs-lookup"><span data-stu-id="940d4-248">For more info about how to add computers to the TrustedHosts list, type `winrm help config`.</span></span>

## <a name="winrm-service-default-configuration-settings"></a><span data-ttu-id="940d4-249">Definições de configuração padrão do serviço WinRM</span><span class="sxs-lookup"><span data-stu-id="940d4-249">WinRM service default configuration settings</span></span>

<span data-ttu-id="940d4-250">A versão do serviço do WinRM tem as seguintes definições de configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="940d4-250">The service version of WinRM has the following default configuration settings.</span></span>

### <a name="rootsddl"></a><span data-ttu-id="940d4-251">RootSDDL</span><span class="sxs-lookup"><span data-stu-id="940d4-251">RootSDDL</span></span>

<span data-ttu-id="940d4-252">Especifica o descritor de segurança que controla o acesso remoto ao ouvinte.</span><span class="sxs-lookup"><span data-stu-id="940d4-252">Specifies the security descriptor that controls remote access to the listener.</span></span> <span data-ttu-id="940d4-253">O padrão é "O:NSG: BAD: P (A;; GA;;; BA) (A;; GR;;; ER) S:P (AU; FA; GA;;; WD) (AU; SA; GWGX;;; WD) ".</span><span class="sxs-lookup"><span data-stu-id="940d4-253">The default is "O:NSG:BAD:P(A;;GA;;;BA)(A;;GR;;;ER)S:P(AU;FA;GA;;;WD)(AU;SA;GWGX;;;WD)".</span></span>

### <a name="maxconcurrentoperations"></a><span data-ttu-id="940d4-254">MaxConcurrentOperations</span><span class="sxs-lookup"><span data-stu-id="940d4-254">MaxConcurrentOperations</span></span>

<span data-ttu-id="940d4-255">O número máximo de operações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="940d4-255">The maximum number of concurrent operations.</span></span> <span data-ttu-id="940d4-256">O padrão é 100.</span><span class="sxs-lookup"><span data-stu-id="940d4-256">The default is 100.</span></span>

<span data-ttu-id="940d4-257">**WinRM 2,0:** A configuração MaxConcurrentOperations é preterida e está definida como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="940d4-257">**WinRM 2.0:** The MaxConcurrentOperations setting is deprecated, and is set to read-only.</span></span> <span data-ttu-id="940d4-258">Essa configuração foi substituída por MaxConcurrentOperationsPerUser.</span><span class="sxs-lookup"><span data-stu-id="940d4-258">This setting has been replaced by MaxConcurrentOperationsPerUser.</span></span>

### <a name="maxconcurrentoperationsperuser"></a><span data-ttu-id="940d4-259">MaxConcurrentOperationsPerUser</span><span class="sxs-lookup"><span data-stu-id="940d4-259">MaxConcurrentOperationsPerUser</span></span>

<span data-ttu-id="940d4-260">Especifica o número máximo de operações simultâneas que qualquer usuário pode abrir remotamente no mesmo sistema.</span><span class="sxs-lookup"><span data-stu-id="940d4-260">Specifies the maximum number of concurrent operations that any user can remotely open on the same system.</span></span> <span data-ttu-id="940d4-261">O padrão é 1500.</span><span class="sxs-lookup"><span data-stu-id="940d4-261">The default is 1500.</span></span>

### <a name="enumerationtimeoutms"></a><span data-ttu-id="940d4-262">EnumerationTimeoutms</span><span class="sxs-lookup"><span data-stu-id="940d4-262">EnumerationTimeoutms</span></span>

<span data-ttu-id="940d4-263">Especifica o tempo limite de ociosidade em milissegundos entre as mensagens de pull.</span><span class="sxs-lookup"><span data-stu-id="940d4-263">Specifies the idle time-out in milliseconds between Pull messages.</span></span> <span data-ttu-id="940d4-264">O padrão é 60000.</span><span class="sxs-lookup"><span data-stu-id="940d4-264">The default is 60000.</span></span>

### <a name="maxconnections"></a><span data-ttu-id="940d4-265">MaxConnections</span><span class="sxs-lookup"><span data-stu-id="940d4-265">MaxConnections</span></span>

<span data-ttu-id="940d4-266">Especifica o número máximo de solicitações ativas que o serviço pode processar simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="940d4-266">Specifies the maximum number of active requests that the service can process simultaneously.</span></span> <span data-ttu-id="940d4-267">O padrão é 300.</span><span class="sxs-lookup"><span data-stu-id="940d4-267">The default is 300.</span></span>

<span data-ttu-id="940d4-268">**WinRM 2,0:** O padrão é 25.</span><span class="sxs-lookup"><span data-stu-id="940d4-268">**WinRM 2.0:** The default is 25.</span></span>

### <a name="maxpacketretrievaltimeseconds"></a><span data-ttu-id="940d4-269">MaxPacketRetrievalTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="940d4-269">MaxPacketRetrievalTimeSeconds</span></span>

<span data-ttu-id="940d4-270">Especifica o período máximo de tempo, em segundos, que o serviço WinRM leva para recuperar um pacote.</span><span class="sxs-lookup"><span data-stu-id="940d4-270">Specifies the maximum length of time, in seconds, the WinRM service takes to retrieve a packet.</span></span> <span data-ttu-id="940d4-271">O padrão é 120 segundos.</span><span class="sxs-lookup"><span data-stu-id="940d4-271">The default is 120 seconds.</span></span>

### <a name="allowunencrypted"></a><span data-ttu-id="940d4-272">AllowUnencrypted</span><span class="sxs-lookup"><span data-stu-id="940d4-272">AllowUnencrypted</span></span>

<span data-ttu-id="940d4-273">Permite que o computador cliente solicite tráfego não criptografado.</span><span class="sxs-lookup"><span data-stu-id="940d4-273">Allows the client computer to request unencrypted traffic.</span></span> <span data-ttu-id="940d4-274">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-274">The default is *False*.</span></span>

### <a name="basic"></a><span data-ttu-id="940d4-275">Básico</span><span class="sxs-lookup"><span data-stu-id="940d4-275">Basic</span></span>

<span data-ttu-id="940d4-276">Permite que o serviço WinRM use a autenticação básica.</span><span class="sxs-lookup"><span data-stu-id="940d4-276">Allows the WinRM service to use Basic authentication.</span></span> <span data-ttu-id="940d4-277">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-277">The default is *False*.</span></span>

### <a name="certificate"></a><span data-ttu-id="940d4-278">Certificado</span><span class="sxs-lookup"><span data-stu-id="940d4-278">Certificate</span></span>

<span data-ttu-id="940d4-279">Permite que o serviço WinRM use a autenticação baseada em certificado do cliente.</span><span class="sxs-lookup"><span data-stu-id="940d4-279">Allows the WinRM service to use client certificate-based authentication.</span></span> <span data-ttu-id="940d4-280">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-280">The default is *False*.</span></span>

### <a name="kerberos"></a><span data-ttu-id="940d4-281">Kerberos</span><span class="sxs-lookup"><span data-stu-id="940d4-281">Kerberos</span></span>

<span data-ttu-id="940d4-282">Permite que o serviço WinRM use a autenticação Kerberos.</span><span class="sxs-lookup"><span data-stu-id="940d4-282">Allows the WinRM service to use Kerberos authentication.</span></span> <span data-ttu-id="940d4-283">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-283">The default is *True*.</span></span>

### <a name="negotiate"></a><span data-ttu-id="940d4-284">Negotiate</span><span class="sxs-lookup"><span data-stu-id="940d4-284">Negotiate</span></span>

<span data-ttu-id="940d4-285">Permite que o serviço WinRM use a autenticação de negociação.</span><span class="sxs-lookup"><span data-stu-id="940d4-285">Allows the WinRM service to use Negotiate authentication.</span></span> <span data-ttu-id="940d4-286">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-286">The default is *True*.</span></span>

### <a name="credssp"></a><span data-ttu-id="940d4-287">CredSSP</span><span class="sxs-lookup"><span data-stu-id="940d4-287">CredSSP</span></span>

<span data-ttu-id="940d4-288">Permite que o serviço WinRM use a autenticação do Credential Security Support Provider (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="940d4-288">Allows the WinRM service to use Credential Security Support Provider (CredSSP) authentication.</span></span> <span data-ttu-id="940d4-289">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-289">The default is *False*.</span></span>

### <a name="cbthardeninglevel"></a><span data-ttu-id="940d4-290">CbtHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="940d4-290">CbtHardeningLevel</span></span>

<span data-ttu-id="940d4-291">Define a política para requisitos de token de associação de canal em solicitações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="940d4-291">Sets the policy for channel-binding token requirements in authentication requests.</span></span> <span data-ttu-id="940d4-292">O padrão é *relaxado*.</span><span class="sxs-lookup"><span data-stu-id="940d4-292">The default is *Relaxed*.</span></span>

### <a name="defaultports"></a><span data-ttu-id="940d4-293">DefaultPorts</span><span class="sxs-lookup"><span data-stu-id="940d4-293">DefaultPorts</span></span>

<span data-ttu-id="940d4-294">Especifica as portas que o serviço WinRM usará para HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="940d4-294">Specifies the ports that the WinRM service will use for either HTTP or HTTPS.</span></span>

<span data-ttu-id="940d4-295">**WinRM 2,0:** A porta HTTP padrão é 5985 e a porta HTTPS padrão é 5986.</span><span class="sxs-lookup"><span data-stu-id="940d4-295">**WinRM 2.0:** The default HTTP port is 5985, and the default HTTPS port is 5986.</span></span>

### <a name="ipv4filter-and-ipv6filter"></a><span data-ttu-id="940d4-296">IPv4Filter e IPv6Filter</span><span class="sxs-lookup"><span data-stu-id="940d4-296">IPv4Filter and IPv6Filter</span></span>

<span data-ttu-id="940d4-297">Especifica os endereços IPv4 ou IPv6 que os ouvintes podem usar.</span><span class="sxs-lookup"><span data-stu-id="940d4-297">Specifies the IPv4 or IPv6 addresses that listeners can use.</span></span> <span data-ttu-id="940d4-298">Os padrões são IPv4Filter = \* e IPv6Filter = \* .</span><span class="sxs-lookup"><span data-stu-id="940d4-298">The defaults are IPv4Filter = \* and IPv6Filter = \*.</span></span>

<span data-ttu-id="940d4-299">**IPv4:** Uma cadeia de caracteres literal IPv4 consiste em quatro números decimais pontilhados, cada um no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="940d4-299">**IPv4:** An IPv4 literal string consists of four dotted decimal numbers, each in the range 0 through 255.</span></span> <span data-ttu-id="940d4-300">Por exemplo: 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="940d4-300">For example: 192.168.0.0.</span></span>

<span data-ttu-id="940d4-301">**IPv6:** Uma cadeia de caracteres literal do IPv6 é colocada entre colchetes e contém números hexadecimais separados por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="940d4-301">**IPv6:** An IPv6 literal string is enclosed in brackets and contains hexadecimal numbers that are separated by colons.</span></span> <span data-ttu-id="940d4-302">Por exemplo:: \[ : 1 \] ou \[ 3ffe: ffff:: 6ECB: 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="940d4-302">For example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

### <a name="enablecompatibilityhttplistener"></a><span data-ttu-id="940d4-303">EnableCompatibilityHttpListener</span><span class="sxs-lookup"><span data-stu-id="940d4-303">EnableCompatibilityHttpListener</span></span>

<span data-ttu-id="940d4-304">Especifica se o ouvinte de HTTP de compatibilidade está habilitado.</span><span class="sxs-lookup"><span data-stu-id="940d4-304">Specifies whether the compatibility HTTP listener is enabled.</span></span> <span data-ttu-id="940d4-305">Se essa configuração for *verdadeira*, o ouvinte escutará na porta 80 além da porta 5985.</span><span class="sxs-lookup"><span data-stu-id="940d4-305">If this setting is *True*, then the listener will listen on port 80 in addition to port 5985.</span></span> <span data-ttu-id="940d4-306">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-306">The default is *False*.</span></span>

### <a name="enablecompatibilityhttpslistener"></a><span data-ttu-id="940d4-307">EnableCompatibilityHttpsListener</span><span class="sxs-lookup"><span data-stu-id="940d4-307">EnableCompatibilityHttpsListener</span></span>

<span data-ttu-id="940d4-308">Especifica se o ouvinte de HTTPS de compatibilidade está habilitado.</span><span class="sxs-lookup"><span data-stu-id="940d4-308">Specifies whether the compatibility HTTPS listener is enabled.</span></span> <span data-ttu-id="940d4-309">Se essa configuração for *verdadeira*, o ouvinte escutará na porta 443 além da porta 5986.</span><span class="sxs-lookup"><span data-stu-id="940d4-309">If this setting is *True*, then the listener will listen on port 443 in addition to port 5986.</span></span> <span data-ttu-id="940d4-310">O padrão é *False*.</span><span class="sxs-lookup"><span data-stu-id="940d4-310">The default is *False*.</span></span>

## <a name="winrs-default-configuration-settings"></a><span data-ttu-id="940d4-311">Definições de configuração padrão do WinRS</span><span class="sxs-lookup"><span data-stu-id="940d4-311">Winrs Default Configuration Settings</span></span>

<span data-ttu-id="940d4-312">`winrm quickconfig` também define as configurações padrão do **WinRS** .</span><span class="sxs-lookup"><span data-stu-id="940d4-312">`winrm quickconfig` also configures **Winrs** default settings.</span></span>

### <a name="allowremoteshellaccess"></a><span data-ttu-id="940d4-313">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="940d4-313">AllowRemoteShellAccess</span></span>

<span data-ttu-id="940d4-314">Permite o acesso a shells remotos.</span><span class="sxs-lookup"><span data-stu-id="940d4-314">Enables access to remote shells.</span></span> <span data-ttu-id="940d4-315">Se você definir esse parâmetro como *false*, as novas conexões de shell remoto serão rejeitadas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="940d4-315">If you set this parameter to *False*, then new remote shell connections will be rejected by the server.</span></span> <span data-ttu-id="940d4-316">O padrão é *True*.</span><span class="sxs-lookup"><span data-stu-id="940d4-316">The default is *True*.</span></span>

### <a name="idletimeout"></a><span data-ttu-id="940d4-317">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="940d4-317">IdleTimeout</span></span>

<span data-ttu-id="940d4-318">Especifica o tempo máximo, em milissegundos, que o shell remoto permanecerá aberto quando não houver nenhuma atividade de usuário no shell remoto.</span><span class="sxs-lookup"><span data-stu-id="940d4-318">Specifies the maximum time, in milliseconds, that the remote shell will remain open when there is no user activity in the remote shell.</span></span> <span data-ttu-id="940d4-319">O shell remoto é excluído automaticamente após o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="940d4-319">The remote shell is automatically deleted after the time that is specified.</span></span>

<span data-ttu-id="940d4-320">**WinRM 2,0:** O padrão é 180000.</span><span class="sxs-lookup"><span data-stu-id="940d4-320">**WinRM 2.0:** The default is 180000.</span></span> <span data-ttu-id="940d4-321">O valor mínimo é 60000.</span><span class="sxs-lookup"><span data-stu-id="940d4-321">The minimum value is 60000.</span></span> <span data-ttu-id="940d4-322">Definir esse valor inferior a 60000 não terá efeito sobre o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="940d4-322">Setting this value lower than 60000 will have no effect on the time-out.</span></span>

### <a name="maxconcurrentusers"></a><span data-ttu-id="940d4-323">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="940d4-323">MaxConcurrentUsers</span></span>

<span data-ttu-id="940d4-324">Especifica o número máximo de usuários que podem executar simultaneamente operações remotas no mesmo computador por meio de um shell remoto.</span><span class="sxs-lookup"><span data-stu-id="940d4-324">Specifies the maximum number of users who can concurrently perform remote operations on the same computer through a remote shell.</span></span> <span data-ttu-id="940d4-325">Novas conexões de shell remoto serão rejeitadas se excederem o limite especificado.</span><span class="sxs-lookup"><span data-stu-id="940d4-325">New remote shell connections will be rejected if they exceed the specified limit.</span></span> <span data-ttu-id="940d4-326">O padrão é 5.</span><span class="sxs-lookup"><span data-stu-id="940d4-326">The default is 5.</span></span>

### <a name="maxshellruntime"></a><span data-ttu-id="940d4-327">MaxShellRunTime</span><span class="sxs-lookup"><span data-stu-id="940d4-327">MaxShellRunTime</span></span>

<span data-ttu-id="940d4-328">Especifica o tempo máximo, em milissegundos, que o comando remoto ou o script pode executar.</span><span class="sxs-lookup"><span data-stu-id="940d4-328">Specifies the maximum time, in milliseconds, that the remote command or script is allowed to execute.</span></span> <span data-ttu-id="940d4-329">O padrão é 28,8 milhões.</span><span class="sxs-lookup"><span data-stu-id="940d4-329">The default is 28800000.</span></span>

<span data-ttu-id="940d4-330">**WinRM 2,0:** A configuração MaxShellRunTime é definida como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="940d4-330">**WinRM 2.0:** The MaxShellRunTime setting is set to read-only.</span></span> <span data-ttu-id="940d4-331">Alterar o valor de MaxShellRunTime não terá nenhum efeito sobre os shells remotos.</span><span class="sxs-lookup"><span data-stu-id="940d4-331">Changing the value for MaxShellRunTime will have no effect on the remote shells.</span></span>

### <a name="maxprocessespershell"></a><span data-ttu-id="940d4-332">MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="940d4-332">MaxProcessesPerShell</span></span>

<span data-ttu-id="940d4-333">Especifica o número máximo de processos que qualquer operação de shell tem permissão para iniciar.</span><span class="sxs-lookup"><span data-stu-id="940d4-333">Specifies the maximum number of processes that any shell operation is allowed to start.</span></span> <span data-ttu-id="940d4-334">Um valor 0 permite um número ilimitado de processos.</span><span class="sxs-lookup"><span data-stu-id="940d4-334">A value of 0 allows for an unlimited number of processes.</span></span> <span data-ttu-id="940d4-335">O padrão é 15.</span><span class="sxs-lookup"><span data-stu-id="940d4-335">The default is 15.</span></span>

### <a name="maxmemorypershellmb"></a><span data-ttu-id="940d4-336">MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="940d4-336">MaxMemoryPerShellMB</span></span>

<span data-ttu-id="940d4-337">Especifica a quantidade máxima de memória alocada por shell, incluindo os processos filho do Shell.</span><span class="sxs-lookup"><span data-stu-id="940d4-337">Specifies the maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="940d4-338">O padrão é 150 MB.</span><span class="sxs-lookup"><span data-stu-id="940d4-338">The default is 150 MB.</span></span>

### <a name="maxshellsperuser"></a><span data-ttu-id="940d4-339">MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="940d4-339">MaxShellsPerUser</span></span>

<span data-ttu-id="940d4-340">Especifica o número máximo de shells simultâneos que um usuário pode abrir remotamente no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="940d4-340">Specifies the maximum number of concurrent shells that any user can remotely open on the same computer.</span></span> <span data-ttu-id="940d4-341">Se essa configuração de política estiver habilitada, o usuário não poderá abrir novos shells remotos se a contagem exceder o limite especificado.</span><span class="sxs-lookup"><span data-stu-id="940d4-341">If this policy setting is enabled, then the user won't be able to open new remote shells if the count exceeds the specified limit.</span></span> <span data-ttu-id="940d4-342">Se esta configuração de política estiver desabilitada ou não estiver configurada, o limite será definido para 5 shells remotos por usuário por padrão.</span><span class="sxs-lookup"><span data-stu-id="940d4-342">If this policy setting is disabled or is not configured, the limit will be set to 5 remote shells per user by default.</span></span>

## <a name="configuring-winrm-with-group-policy"></a><span data-ttu-id="940d4-343">Configurando o WinRM com o Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="940d4-343">Configuring WinRM with Group Policy</span></span>

<span data-ttu-id="940d4-344">Use o editor de Política de Grupo para configurar o shell remoto do Windows e o WinRM para computadores em sua empresa.</span><span class="sxs-lookup"><span data-stu-id="940d4-344">Use the Group Policy editor to configure Windows Remote Shell and WinRM for computers in your enterprise.</span></span>

### <a name="to-configure-with-group-policy"></a><span data-ttu-id="940d4-345">Para configurar com Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="940d4-345">To configure with Group Policy</span></span>

1. <span data-ttu-id="940d4-346">Abra uma janela de Prompt de comando como administrador.</span><span class="sxs-lookup"><span data-stu-id="940d4-346">Open a Command Prompt window as an administrator.</span></span>
2. <span data-ttu-id="940d4-347">No prompt de comando, digite `gpedit.msc` .</span><span class="sxs-lookup"><span data-stu-id="940d4-347">At the Command Prompt, type `gpedit.msc`.</span></span> <span data-ttu-id="940d4-348">A janela **Editor de objeto de política de grupo** é aberta.</span><span class="sxs-lookup"><span data-stu-id="940d4-348">The **Group Policy Object Editor** window opens.</span></span>
3. <span data-ttu-id="940d4-349">Localize o **gerenciamento remoto do Windows** e o **Windows Remote Shell** política de grupo Objects (GPO) em **configuração do computador \\ modelos administrativos componentes do \\ Windows**.</span><span class="sxs-lookup"><span data-stu-id="940d4-349">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4. <span data-ttu-id="940d4-350">Na guia **estendida** , selecione uma configuração para ver uma descrição.</span><span class="sxs-lookup"><span data-stu-id="940d4-350">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="940d4-351">Clique duas vezes em uma configuração para editá-la.</span><span class="sxs-lookup"><span data-stu-id="940d4-351">Double click a setting to edit it.</span></span>

## <a name="windows-firewall-and-winrm-20-ports"></a><span data-ttu-id="940d4-352">Portas do firewall do Windows e do WinRM 2,0</span><span class="sxs-lookup"><span data-stu-id="940d4-352">Windows Firewall and WinRM 2.0 ports</span></span>

<span data-ttu-id="940d4-353">A partir do WinRM 2,0, as portas de ouvinte padrão configuradas pelo `Winrm quickconfig` são a porta 5985 para transporte http e a porta 5986 para https.</span><span class="sxs-lookup"><span data-stu-id="940d4-353">Starting in WinRM 2.0, the default listener ports configured by `Winrm quickconfig` are port 5985 for HTTP transport, and port 5986 for HTTPS.</span></span> <span data-ttu-id="940d4-354">Os ouvintes do WinRM podem ser configurados em qualquer porta arbitrária.</span><span class="sxs-lookup"><span data-stu-id="940d4-354">WinRM listeners can be configured on any arbitrary port.</span></span>

<span data-ttu-id="940d4-355">Se um computador for atualizado para o WinRM 2,0, os ouvintes configurados anteriormente serão migrados e ainda receberão o tráfego.</span><span class="sxs-lookup"><span data-stu-id="940d4-355">If a computer is upgraded to WinRM 2.0, the previously configured listeners are migrated, and still receive traffic.</span></span>

## <a name="winrm-installation-and-configuration-notes"></a><span data-ttu-id="940d4-356">Notas de instalação e configuração do WinRM</span><span class="sxs-lookup"><span data-stu-id="940d4-356">WinRM installation and configuration notes</span></span>

<span data-ttu-id="940d4-357">O WinRM não depende de nenhum outro serviço, exceto WinHttp.</span><span class="sxs-lookup"><span data-stu-id="940d4-357">WinRM isn't dependent on any other service except WinHttp.</span></span> <span data-ttu-id="940d4-358">Se o serviço de administração do IIS estiver instalado no mesmo computador, você poderá ver mensagens que indicam que o WinRM não pode ser carregado antes de Serviços de Informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="940d4-358">If the IIS Admin Service is installed on the same computer, then you might see messages that indicate that WinRM can't be loaded before Internet Information Services (IIS).</span></span> <span data-ttu-id="940d4-359">No entanto, o WinRM não depende realmente do IIS &mdash; que essas mensagens ocorrem porque a ordem de carregamento garante que o serviço IIS seja iniciado antes do serviço http.</span><span class="sxs-lookup"><span data-stu-id="940d4-359">However, WinRM doesn't actually depend on IIS&mdash;those messages occur because the load order ensures that the IIS service starts before the HTTP service.</span></span> <span data-ttu-id="940d4-360">O WinRM requer que `WinHTTP.dll` seja registrado.</span><span class="sxs-lookup"><span data-stu-id="940d4-360">WinRM does require that `WinHTTP.dll` be registered.</span></span>

<span data-ttu-id="940d4-361">Se o cliente de firewall do ISA2004 estiver instalado no computador, ele poderá fazer com que um cliente do Web Services para gerenciamento (WS-Management) pare de responder.</span><span class="sxs-lookup"><span data-stu-id="940d4-361">If the ISA2004 firewall client is installed on the computer, then it can cause a Web Services for Management (WS-Management) client to stop responding.</span></span> <span data-ttu-id="940d4-362">Para evitar esse problema, instale o ISA2004 firewall SP1.</span><span class="sxs-lookup"><span data-stu-id="940d4-362">To avoid this issue, install ISA2004 Firewall SP1.</span></span>

<span data-ttu-id="940d4-363">Se dois serviços de escuta com endereços IP diferentes estiverem configurados com o mesmo número de porta e nome do computador, o WinRM escutará ou receberá mensagens em apenas um endereço.</span><span class="sxs-lookup"><span data-stu-id="940d4-363">If two listener services with different IP addresses are configured with the same port number and computer name, then WinRM listens or receives messages on only one address.</span></span> <span data-ttu-id="940d4-364">Isso ocorre porque os prefixos de URL usados pelo protocolo WS-Management são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="940d4-364">This is because the URL prefixes used by the WS-Management protocol are the same.</span></span>

## <a name="ipmi-driver-and-provider-installation-notes"></a><span data-ttu-id="940d4-365">Notas de instalação do driver e do provedor IPMI</span><span class="sxs-lookup"><span data-stu-id="940d4-365">IPMI driver and provider installation notes</span></span>

<span data-ttu-id="940d4-366">O driver pode não detectar a existência de drivers IPMI que não são da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="940d4-366">The driver might not detect the existence of IPMI drivers that are not from Microsoft.</span></span> <span data-ttu-id="940d4-367">Se o driver não for iniciado, talvez seja necessário desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="940d4-367">If the driver fails to start, then you might need to disable it.</span></span>

<span data-ttu-id="940d4-368">Se os recursos do [BMC (Baseboard Management Controller)](./windows-remote-management-glossary.md#b) aparecerem no BIOS do sistema, a ACPI (plug and Play) detectará o hardware do BMC e instalará automaticamente o driver IPMI.</span><span class="sxs-lookup"><span data-stu-id="940d4-368">If the [baseboard management controller (BMC)](./windows-remote-management-glossary.md#b) resources appear in the system BIOS, then ACPI (Plug and Play) detects the BMC hardware, and automatically installs the IPMI driver.</span></span> <span data-ttu-id="940d4-369">Plug and Play suporte pode não estar presente em todos os BMCs.</span><span class="sxs-lookup"><span data-stu-id="940d4-369">Plug and Play support might not be present in all BMCs.</span></span> <span data-ttu-id="940d4-370">Se o BMC for detectado pelo Plug and Play, um dispositivo desconhecido aparecerá em Gerenciador de Dispositivos antes de o componente de gerenciamento de hardware ser instalado.</span><span class="sxs-lookup"><span data-stu-id="940d4-370">If the BMC is detected by Plug and Play, then an Unknown Device appears in Device Manager before the Hardware Management component is installed.</span></span> <span data-ttu-id="940d4-371">Quando o driver é instalado, um novo componente, o dispositivo compatível com IPMI genérico do Microsoft ACPI, aparece em Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="940d4-371">When the driver is installed, a new component, the Microsoft ACPI Generic IPMI Compliant Device, appears in Device Manager.</span></span>

<span data-ttu-id="940d4-372">Se o seu sistema não detectar automaticamente o BMC e instalar o driver, mas um BMC foi detectado durante o processo de instalação, você deverá criar o dispositivo BMC.</span><span class="sxs-lookup"><span data-stu-id="940d4-372">If your system doesn't automatically detect the BMC and install the driver, but a BMC was detected during the setup process, then you must create the BMC device.</span></span> <span data-ttu-id="940d4-373">Para fazer isso, digite o seguinte comando no prompt de comando: `Rundll32 ipmisetp.dll, AddTheDevice` .</span><span class="sxs-lookup"><span data-stu-id="940d4-373">To do this, type the following command at a command prompt: `Rundll32 ipmisetp.dll, AddTheDevice`.</span></span> <span data-ttu-id="940d4-374">Depois que esse comando é executado, o dispositivo IPMI é criado e aparece em Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="940d4-374">After this command is executed, the IPMI device is created, and it appears in Device Manager.</span></span> <span data-ttu-id="940d4-375">Se você desinstalar o componente de gerenciamento de hardware, o dispositivo será removido.</span><span class="sxs-lookup"><span data-stu-id="940d4-375">If you uninstall the Hardware Management component, then the device is removed.</span></span>

<span data-ttu-id="940d4-376">Para obter mais informações, consulte [introdução ao gerenciamento de hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="940d4-376">For more information, see [Hardware Management Introduction](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).</span></span>

<span data-ttu-id="940d4-377">O provedor de IPMI coloca as classes de hardware no [namespace](/windows/desktop/WmiSdk/gloss-n) de **\\ hardware raiz** do WMI.</span><span class="sxs-lookup"><span data-stu-id="940d4-377">The IPMI provider places the hardware classes in the **root\\hardware** [namespace](/windows/desktop/WmiSdk/gloss-n) of WMI.</span></span> <span data-ttu-id="940d4-378">Para obter mais informações sobre as classes de hardware, consulte [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="940d4-378">For more information about the hardware classes, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="940d4-379">Para obter mais informações sobre *namespaces* WMI, consulte [arquitetura WMI](/windows/desktop/WmiSdk/wmi-architecture).</span><span class="sxs-lookup"><span data-stu-id="940d4-379">For more information about WMI *namespaces*, see [WMI Architecture](/windows/desktop/WmiSdk/wmi-architecture).</span></span>

## <a name="wmi-plug-in-configuration-notes"></a><span data-ttu-id="940d4-380">Observações de configuração de plug-in WMI</span><span class="sxs-lookup"><span data-stu-id="940d4-380">WMI plug-in configuration notes</span></span>

<span data-ttu-id="940d4-381">A partir do Windows 8 e do Windows Server 2012, os [plug-ins WMI](./windows-remote-management-glossary.md#w) têm suas próprias configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="940d4-381">Beginning with Windows 8 and Windows Server 2012, [WMI plug-ins](./windows-remote-management-glossary.md#w) have their own security configurations.</span></span> <span data-ttu-id="940d4-382">Para que um usuário normal ou de energia (não administrador) possa usar o *plug-in WMI*, você precisa habilitar o acesso para esse usuário após a configuração do [ouvinte](./windows-remote-management-glossary.md#l) .</span><span class="sxs-lookup"><span data-stu-id="940d4-382">For a normal or power (non-administrator) user to be able to use the *WMI plug-in*, you need to enable access for that user after the [listener](./windows-remote-management-glossary.md#l) has been configured.</span></span> <span data-ttu-id="940d4-383">Primeiro, você deve configurar o usuário para acesso remoto ao [WMI](./windows-remote-management-glossary.md#w) por meio de uma destas etapas.</span><span class="sxs-lookup"><span data-stu-id="940d4-383">First, you must set up the user for remote access to [WMI](./windows-remote-management-glossary.md#w) through one of these steps.</span></span>

- <span data-ttu-id="940d4-384">Execute `lusrmgr.msc` para adicionar o usuário ao grupo **WinRMRemoteWMIUsers \_ \_** na janela **usuários e grupos locais** ou</span><span class="sxs-lookup"><span data-stu-id="940d4-384">Run `lusrmgr.msc` to add the user to the **WinRMRemoteWMIUsers\_\_** group in the **Local Users and Groups** window, or</span></span>
- <span data-ttu-id="940d4-385">Use a ferramenta de linha de comando **WinRM** para configurar o descritor de segurança para o [*namespace*](./windows-remote-management-glossary.md#n) do [plug-in do WMI](./windows-remote-management-glossary.md#w), da seguinte maneira: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .</span><span class="sxs-lookup"><span data-stu-id="940d4-385">use the **winrm** command-line tool to configure the security descriptor for the [*namespace*](./windows-remote-management-glossary.md#n) of the [WMI plug-in](./windows-remote-management-glossary.md#w), as follows: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace`.</span></span>

<span data-ttu-id="940d4-386">Quando a interface do usuário for exibida, adicione o usuário.</span><span class="sxs-lookup"><span data-stu-id="940d4-386">When the user interface appears, add the user.</span></span>

<span data-ttu-id="940d4-387">Depois de configurar o usuário para acesso remoto ao [WMI](./windows-remote-management-glossary.md#w), você deve configurar o *WMI* para permitir que o usuário acesse o plug-in.</span><span class="sxs-lookup"><span data-stu-id="940d4-387">After setting up the user for remote access to [WMI](./windows-remote-management-glossary.md#w), you must set up *WMI* to allow the user to access the plug-in.</span></span> <span data-ttu-id="940d4-388">Para fazer isso, execute `wmimgmt.msc` para modificar a segurança do *WMI* para o [namespace](./windows-remote-management-glossary.md#n) a ser acessado na janela **controle WMI** .</span><span class="sxs-lookup"><span data-stu-id="940d4-388">To do this, run `wmimgmt.msc` to modify the *WMI* security for the [namespace](./windows-remote-management-glossary.md#n) to be accessed in the **WMI Control** window.</span></span>

<span data-ttu-id="940d4-389">A maioria das classes WMI para gerenciamento está no namespace **raiz \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="940d4-389">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span>