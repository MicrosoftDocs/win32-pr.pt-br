---
title: Aprimoramentos na infraestrutura do shell remoto
description: Gerenciamento Remoto do Windows versão 2,0 (WinRM 2,0) oferece muitos aprimoramentos na infraestrutura do shell remoto.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c67752222f1ca969ea254164a25144168d1eb3
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/24/2020
ms.locfileid: "104007029"
---
# <a name="remote-shell-infrastructure-improvements"></a><span data-ttu-id="35a8f-103">Aprimoramentos na infraestrutura do shell remoto</span><span class="sxs-lookup"><span data-stu-id="35a8f-103">Remote Shell Infrastructure Improvements</span></span>

<span data-ttu-id="35a8f-104">Gerenciamento Remoto do Windows versão 2,0 (WinRM 2,0) oferece muitos aprimoramentos na infraestrutura do shell remoto.</span><span class="sxs-lookup"><span data-stu-id="35a8f-104">Windows Remote Management version 2.0 (WinRM 2.0) offers many remote shell infrastructure improvements.</span></span> <span data-ttu-id="35a8f-105">Os tópicos a seguir descrevem esses aprimoramentos em detalhes:</span><span class="sxs-lookup"><span data-stu-id="35a8f-105">The following topics describe these improvements in detail:</span></span>

-   [<span data-ttu-id="35a8f-106">Suporte a vários saltos</span><span class="sxs-lookup"><span data-stu-id="35a8f-106">Multi-Hop Support</span></span>](multi-hop-support.md)
-   [<span data-ttu-id="35a8f-107">Gerenciamento de cota para shells remotos</span><span class="sxs-lookup"><span data-stu-id="35a8f-107">Quota Management for Remote Shells</span></span>](quotas.md)

<span data-ttu-id="35a8f-108">Uma das melhorias na infra-estrutura de shell remoto do WinRM é a adição de um Gerenciador de Shell mais robusto que mantém informações de shell específicas do usuário.</span><span class="sxs-lookup"><span data-stu-id="35a8f-108">One of the improvements to the WinRM remote shell infrastructure is the addition of a more robust shell manager that maintains user-specific shell information.</span></span> <span data-ttu-id="35a8f-109">Os usuários do WinRM podem criar shells em computadores remotos para executar comandos ou scripts.</span><span class="sxs-lookup"><span data-stu-id="35a8f-109">WinRM users can create shells on remote computers to run commands or scripts.</span></span> <span data-ttu-id="35a8f-110">Além disso, os usuários podem criar vários shells em um computador.</span><span class="sxs-lookup"><span data-stu-id="35a8f-110">In addition, users can create multiple shells on a computer.</span></span> <span data-ttu-id="35a8f-111">Os usuários e administradores precisam da capacidade de gerenciar shells.</span><span class="sxs-lookup"><span data-stu-id="35a8f-111">Users and administrators both need the ability to manage shells.</span></span> <span data-ttu-id="35a8f-112">Os usuários podem enumerar, obter e excluir os shells que criaram.</span><span class="sxs-lookup"><span data-stu-id="35a8f-112">Users can enumerate, get, and delete the shells that they have created.</span></span> <span data-ttu-id="35a8f-113">Os administradores podem enumerar todos os shells ativos e recuperar detalhes sobre shells específicos em um host local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="35a8f-113">Administrators can enumerate over all active shells and retrieve details about specific shells on a local or remote host.</span></span> <span data-ttu-id="35a8f-114">Os administradores também podem excluir qualquer Shell ativo em um host local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="35a8f-114">Administrators can also delete any active shells on a local or remote host.</span></span>

<span data-ttu-id="35a8f-115">Quando um usuário ou administrador enumera os shells ativos, as informações a seguir podem ser retornadas pelo serviço WinRM.</span><span class="sxs-lookup"><span data-stu-id="35a8f-115">When a user or administrator enumerates the active shells, the following information can be returned by the WinRM service.</span></span>

<dl> <dt>

<span data-ttu-id="35a8f-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span><span class="sxs-lookup"><span data-stu-id="35a8f-116"><span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-117">Especifica o identificador exclusivo para o Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-117">Specifies the unique identifier for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variáveis de ambiente</span><span class="sxs-lookup"><span data-stu-id="35a8f-118"><span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Environment variables</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-119">Especifica qualquer variável de ambiente definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="35a8f-119">Specifies any environment variables set by the user.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="35a8f-120"><span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-121">Especifica o diretório inicial para o Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-121">Specifies the starting directory for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span><span class="sxs-lookup"><span data-stu-id="35a8f-122"><span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>ResourceURI</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-123">Especifica o URI de recurso para a operação de Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-123">Specifies the resource URI for the shell operation.</span></span> <span data-ttu-id="35a8f-124">O URI de recurso pode ser usado para recuperar a configuração de plug-in que é específica para a instância do Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-124">The resource URI can be used to retrieve plug-in configuration that is specific to the shell instance.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="35a8f-125"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-126">Especifica a duração máxima, em milissegundos, que o Shell permanecerá aberto sem nenhuma solicitação.</span><span class="sxs-lookup"><span data-stu-id="35a8f-126">Specifies the maximum duration, in milliseconds, that the shell will stay open without any request.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span><span class="sxs-lookup"><span data-stu-id="35a8f-127"><span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-128">Especifica os fluxos de entrada para o Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-128">Specifies the input streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span><span class="sxs-lookup"><span data-stu-id="35a8f-129"><span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-130">Especifica os fluxos de saída para o Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-130">Specifies the output streams for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Hora de criação do Shell</span><span class="sxs-lookup"><span data-stu-id="35a8f-131"><span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Shell creation time</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-132">Especifica o carimbo de data/hora de criação do Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-132">Specifies the creation timestamp for the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>Tempo ocioso</span><span class="sxs-lookup"><span data-stu-id="35a8f-133"><span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-134">Especifica a duração, em milissegundos, que o Shell esteve ocioso.</span><span class="sxs-lookup"><span data-stu-id="35a8f-134">Specifies the duration, in milliseconds, that the shell has been idle.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>ID</span><span class="sxs-lookup"><span data-stu-id="35a8f-135"><span id="UserId"></span><span id="userid"></span><span id="USERID"></span>UserId</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-136">Especifica a ID de usuário.</span><span class="sxs-lookup"><span data-stu-id="35a8f-136">Specifies the user ID.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nome do host ou endereço IP</span><span class="sxs-lookup"><span data-stu-id="35a8f-137"><span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Hostname or IP address</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-138">Especifica o nome do host ou o endereço IP do computador que criou o Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-138">Specifies either the host name or IP address of the computer that created the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Uso de memória do Shell</span><span class="sxs-lookup"><span data-stu-id="35a8f-139"><span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Shell memory usage</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-140">Especifica a quantidade de memória que foi usada pelo shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-140">Specifies the amount of memory that has been used by the shell.</span></span>

</dd> <dt>

<span data-ttu-id="35a8f-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Número de processos</span><span class="sxs-lookup"><span data-stu-id="35a8f-141"><span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Number of processes</span></span>
</dt> <dd>

<span data-ttu-id="35a8f-142">Especifica o número de processos que foram criados pelo shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-142">Specifies the number of processes that have been created by the shell.</span></span>

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a><span data-ttu-id="35a8f-143">Enumerando um shell em um host local</span><span class="sxs-lookup"><span data-stu-id="35a8f-143">Enumerating a Shell on a Local Host</span></span>

<span data-ttu-id="35a8f-144">O comando a seguir demonstra como usar o utilitário WinRM para enumerar shells em um cliente WinRM: **WinRM Enumerate Shell**.</span><span class="sxs-lookup"><span data-stu-id="35a8f-144">The following command demonstrates how to use the winrm utility to enumerate shells on a WinRM client: **winrm enumerate shell**.</span></span>

<span data-ttu-id="35a8f-145">O exemplo com base em texto a seguir exibe a saída para a enumeração do Shell:</span><span class="sxs-lookup"><span data-stu-id="35a8f-145">The following text-based example displays the output for shell enumeration:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

<span data-ttu-id="35a8f-146">Para obter mais informações, consulte a ajuda online fornecida executando o seguinte comando: **WinRM Enumerate-?**.</span><span class="sxs-lookup"><span data-stu-id="35a8f-146">For more information, see the online help provided by running the following command: **winrm enumerate -?**.</span></span>

## <a name="retrieving-information-about-a-specific-shell"></a><span data-ttu-id="35a8f-147">Recuperando informações sobre um shell específico</span><span class="sxs-lookup"><span data-stu-id="35a8f-147">Retrieving Information About a Specific Shell</span></span>

<span data-ttu-id="35a8f-148">Um administrador ou usuário também pode usar o identificador ShellId para recuperar informações sobre o Shell.</span><span class="sxs-lookup"><span data-stu-id="35a8f-148">An administrator or user can also use the ShellId identifier to retrieve information about the shell.</span></span> <span data-ttu-id="35a8f-149">O comando a seguir demonstra como usar o utilitário WinRM para obter informações sobre um shell específico: **WinRM Get Shell? ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span><span class="sxs-lookup"><span data-stu-id="35a8f-149">The following command demonstrates how to use the winrm utility to get information about a specific shell: **winrm get shell?ShellId=0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.</span></span>

<span data-ttu-id="35a8f-150">O exemplo com base em texto a seguir exibe a saída das informações do Shell:</span><span class="sxs-lookup"><span data-stu-id="35a8f-150">The following text-based example displays the output for shell information:</span></span>

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

<span data-ttu-id="35a8f-151">Para obter mais informações, consulte a ajuda online fornecida pelo seguinte comando: **WinRM Get-?**.</span><span class="sxs-lookup"><span data-stu-id="35a8f-151">For more information, see the online help provided by the following command: **winrm get -?**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35a8f-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35a8f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35a8f-153">Suporte a vários saltos</span><span class="sxs-lookup"><span data-stu-id="35a8f-153">Multi-Hop Support</span></span>](multi-hop-support.md)
</dt> <dt>

[<span data-ttu-id="35a8f-154">Gerenciamento de cota para shells remotos</span><span class="sxs-lookup"><span data-stu-id="35a8f-154">Quota Management for Remote Shells</span></span>](quotas.md)
</dt> <dt>

[<span data-ttu-id="35a8f-155">Referência gerenciada para comandos WS-Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="35a8f-155">Managed Reference for WS-Management PowerShell Commands</span></span>](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




