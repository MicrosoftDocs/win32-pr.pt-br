---
title: Gerenciamento de cota para shells remotos
description: O gerenciamento de cotas permite que os usuários gerenciem recursos do sistema com mais eficiência.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292629"
---
# <a name="quota-management-for-remote-shells"></a><span data-ttu-id="53316-103">Gerenciamento de cota para shells remotos</span><span class="sxs-lookup"><span data-stu-id="53316-103">Quota Management for Remote Shells</span></span>

<span data-ttu-id="53316-104">O gerenciamento de cotas permite que os usuários gerenciem recursos do sistema com mais eficiência.</span><span class="sxs-lookup"><span data-stu-id="53316-104">Quota management allows users to manage system resources more efficiently.</span></span> <span data-ttu-id="53316-105">O Gerenciamento Remoto do Windows (WinRM) adicionou um conjunto específico de cotas que fornecem uma melhor qualidade de serviço, ajudam a evitar problemas de negação de serviço e aloca recursos de servidor a usuários simultâneos.</span><span class="sxs-lookup"><span data-stu-id="53316-105">Windows Remote Management (WinRM) has added a specific set of quotas that provide a better quality of service, help prevent denial of service issues, and allocate server resources to concurrent users.</span></span> <span data-ttu-id="53316-106">O conjunto de cotas do WinRM é baseado na infraestrutura de cota que é implementada para o serviço de Serviços de Informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="53316-106">The WinRM quota set is based on the quota infrastructure that is implemented for the Internet Information Services (IIS) service.</span></span>

<span data-ttu-id="53316-107">A implementação de cotas ajudará a evitar a degradação do desempenho e a negação de problemas de serviço fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="53316-107">Implementing quotas will help to prevent performance degradation and denial of service issues by doing the following:</span></span>

-   <span data-ttu-id="53316-108">Limitando o número de shells e processos de shell que um usuário pode criar</span><span class="sxs-lookup"><span data-stu-id="53316-108">Limiting the number of shells and shell processes that a user can create</span></span>
-   <span data-ttu-id="53316-109">Limitando o número máximo de usuários simultâneos</span><span class="sxs-lookup"><span data-stu-id="53316-109">Limiting the maximum number of concurrent users</span></span>
-   <span data-ttu-id="53316-110">Gerenciando a quantidade de memória alocada para um shell</span><span class="sxs-lookup"><span data-stu-id="53316-110">Managing the amount of memory that is allocated to a shell</span></span>
-   <span data-ttu-id="53316-111">Definindo um tempo limite para shells que estão inativos</span><span class="sxs-lookup"><span data-stu-id="53316-111">Setting a time-out for shells that are inactive</span></span>

## <a name="quota-settings"></a><span data-ttu-id="53316-112">Configurações de cota</span><span class="sxs-lookup"><span data-stu-id="53316-112">Quota Settings</span></span>

<span data-ttu-id="53316-113">As cotas a seguir precisam ser impostas para o gerenciamento remoto de Shell.</span><span class="sxs-lookup"><span data-stu-id="53316-113">The following quotas need to be enforced for remote shell management.</span></span> <span data-ttu-id="53316-114">Essas cotas podem ser configuradas por meio do utilitário WinRM ou por meio de configurações de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="53316-114">These quotas can be configured through the winrm utility or through Group Policy settings.</span></span> <span data-ttu-id="53316-115">As configurações definidas por um Política de Grupo substituem as cotas definidas pelo utilitário WinRM.</span><span class="sxs-lookup"><span data-stu-id="53316-115">Settings configured by a Group Policy supersede the quotas set by the winrm utility.</span></span> <span data-ttu-id="53316-116">Para obter mais informações sobre como definir políticas de grupo para o WinRM, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="53316-116">For more information about setting Group Policies for WinRM, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<dl> <dt>

<span data-ttu-id="53316-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="53316-117"><span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout</span></span>
</dt> <dd>

<span data-ttu-id="53316-118">O tempo máximo em milissegundos antes que um shell remoto inativo seja excluído.</span><span class="sxs-lookup"><span data-stu-id="53316-118">The maximum time in milliseconds before an inactive remote shell is deleted.</span></span> <span data-ttu-id="53316-119">O padrão é 180000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="53316-119">The default is 180000 milliseconds.</span></span> <span data-ttu-id="53316-120">O tempo mínimo é de 1000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="53316-120">The minimum time is 1000 milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="53316-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span><span class="sxs-lookup"><span data-stu-id="53316-121"><span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell</span></span>
</dt> <dd>

<span data-ttu-id="53316-122">O número máximo de processos permitidos por shell, incluindo os processos filho do Shell.</span><span class="sxs-lookup"><span data-stu-id="53316-122">The maximum number of processes allowed per shell, including the shell's child processes.</span></span> <span data-ttu-id="53316-123">O padrão é 25.</span><span class="sxs-lookup"><span data-stu-id="53316-123">The default is 25.</span></span>

</dd> <dt>

<span data-ttu-id="53316-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span><span class="sxs-lookup"><span data-stu-id="53316-124"><span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB</span></span>
</dt> <dd>

<span data-ttu-id="53316-125">A quantidade máxima de memória alocada por shell, incluindo os processos filho do Shell.</span><span class="sxs-lookup"><span data-stu-id="53316-125">The maximum amount of memory allocated per shell, including the shell's child processes.</span></span> <span data-ttu-id="53316-126">O padrão é 1024 MB.</span><span class="sxs-lookup"><span data-stu-id="53316-126">The default is 1024 MB.</span></span>

> [!Note]  
> <span data-ttu-id="53316-127">O comportamento não será suportado se MaxMemoryPerShellMB for definido como um valor menor que o padrão.</span><span class="sxs-lookup"><span data-stu-id="53316-127">The behavior is unsupported if the MaxMemoryPerShellMB is set to a value that is less than the default.</span></span>

 

</dd> <dt>

<span data-ttu-id="53316-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span><span class="sxs-lookup"><span data-stu-id="53316-128"><span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser</span></span>
</dt> <dd>

<span data-ttu-id="53316-129">O número máximo de shells por usuário.</span><span class="sxs-lookup"><span data-stu-id="53316-129">The maximum number of shells per user.</span></span> <span data-ttu-id="53316-130">O padrão é 30.</span><span class="sxs-lookup"><span data-stu-id="53316-130">The default is 30.</span></span>

</dd> <dt>

<span data-ttu-id="53316-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="53316-131"><span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers</span></span>
</dt> <dd>

<span data-ttu-id="53316-132">O número máximo de usuários simultâneos que podem abrir shells.</span><span class="sxs-lookup"><span data-stu-id="53316-132">The maximum number of concurrent users who can open shells.</span></span> <span data-ttu-id="53316-133">O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="53316-133">The default is 10.</span></span>

</dd> </dl>

## <a name="deprecated-quotas"></a><span data-ttu-id="53316-134">Cotas preteridas</span><span class="sxs-lookup"><span data-stu-id="53316-134">Deprecated Quotas</span></span>

<span data-ttu-id="53316-135">O WinRM 2,0 define a cota de MaxShellRunTime como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="53316-135">WinRM 2.0 sets the MaxShellRunTime quota to read-only.</span></span> <span data-ttu-id="53316-136">Alterar o valor dessa cota não terá nenhum efeito nos shells remotos.</span><span class="sxs-lookup"><span data-stu-id="53316-136">Changing the value for this quota will have no effect on the remote shells.</span></span>

## <a name="retrieving-quota-configuration-information"></a><span data-ttu-id="53316-137">Recuperando informações de configuração de cota</span><span class="sxs-lookup"><span data-stu-id="53316-137">Retrieving Quota Configuration Information</span></span>

<span data-ttu-id="53316-138">Para verificar as definições de configuração de cota, digite **WinRM Get WinRM/config**.</span><span class="sxs-lookup"><span data-stu-id="53316-138">To check the quota configuration settings, type **winrm get winrm/config**.</span></span>

<span data-ttu-id="53316-139">O trecho a seguir é um exemplo baseado em texto de uma configuração do WinRM com as configurações de cota padrão.</span><span class="sxs-lookup"><span data-stu-id="53316-139">The following snippet is a text-based example of a WinRM configuration with the default quota settings.</span></span>

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a><span data-ttu-id="53316-140">Configurando cotas do Shell</span><span class="sxs-lookup"><span data-stu-id="53316-140">Configuring Shell Quotas</span></span>

<span data-ttu-id="53316-141">As cotas podem ser definidas por meio de uma configuração de Política de Grupo ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="53316-141">Quotas can be set through a Group Policy setting or manually.</span></span> <span data-ttu-id="53316-142">Para obter mais informações sobre definições de configuração específicas, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="53316-142">For more information about specific configuration settings, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

<span data-ttu-id="53316-143">**Para definir uma cota com Política de Grupo**</span><span class="sxs-lookup"><span data-stu-id="53316-143">**To set a quota with Group Policy**</span></span>

1.  <span data-ttu-id="53316-144">Abra uma janela de Prompt de comando como administrador.</span><span class="sxs-lookup"><span data-stu-id="53316-144">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="53316-145">No prompt de comando, digite **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="53316-145">At the Command Prompt, type **gpedit.msc**.</span></span> <span data-ttu-id="53316-146">A janela **Editor de objeto de política de grupo** é aberta.</span><span class="sxs-lookup"><span data-stu-id="53316-146">The **Group Policy Object Editor** window opens.</span></span>
3.  <span data-ttu-id="53316-147">Localize o **gerenciamento remoto do Windows** e o **Windows Remote Shell** política de grupo Objects (GPO) em **configuração do computador \\ modelos administrativos componentes do \\ Windows**.</span><span class="sxs-lookup"><span data-stu-id="53316-147">Find the **Windows Remote Management** and **Windows Remote Shell** Group Policy Objects (GPO) under **Computer Configuration\\Administrative Templates\\Windows Components**.</span></span>
4.  <span data-ttu-id="53316-148">Na guia **estendida** , selecione uma configuração para ver uma descrição.</span><span class="sxs-lookup"><span data-stu-id="53316-148">On the **Extended** tab, select a setting to see a description.</span></span> <span data-ttu-id="53316-149">Clique duas vezes em uma configuração para editá-la.</span><span class="sxs-lookup"><span data-stu-id="53316-149">Double click a setting to edit it.</span></span>

<span data-ttu-id="53316-150">**Para definir uma cota manualmente**</span><span class="sxs-lookup"><span data-stu-id="53316-150">**To set a quota manually**</span></span>

1.  <span data-ttu-id="53316-151">Abra uma janela de Prompt de comando como administrador.</span><span class="sxs-lookup"><span data-stu-id="53316-151">Open a Command Prompt window as an administrator.</span></span>
2.  <span data-ttu-id="53316-152">No prompt de comando, digite **WinRM Set WinRM/config/WinRS ' @ { ***<Quota>*** = " ***<Value>*** "} '**</span><span class="sxs-lookup"><span data-stu-id="53316-152">At the Command Prompt, type **winrm set winrm/config/winrs '@{***<Quota>***="***<Value>***"}'**</span></span>

<span data-ttu-id="53316-153">Por exemplo, para aumentar o número máximo de shells por usuário de 5 para 7, digite **WinRM Set WinRM/config/WinRS ' @ {MaxShellsPerUser = "7"} '**.</span><span class="sxs-lookup"><span data-stu-id="53316-153">For example, to increase the maximum number of shells per user from 5 to 7, type **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.</span></span>

 

 




