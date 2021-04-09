---
description: Cria um novo serviço gerenciado pelo driver do sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Método Create da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089678"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="f7d13-103">Criar método da \_ classe systemdrive do Win32</span><span class="sxs-lookup"><span data-stu-id="f7d13-103">Create method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="f7d13-104">O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço gerenciado pelo driver do sistema.</span><span class="sxs-lookup"><span data-stu-id="f7d13-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service managed by the system driver.</span></span> <span data-ttu-id="f7d13-105">O parâmetro do grupo de *\_ pedidos do Win32* representa um agrupamento de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="f7d13-105">The *Win32\_LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="f7d13-106">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="f7d13-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="f7d13-107">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="f7d13-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="f7d13-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f7d13-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f7d13-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f7d13-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d13-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7d13-110">Syntax</span></span>


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="f7d13-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7d13-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d13-112">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-113">Nome do serviço a ser instalado para o método **Create** .</span><span class="sxs-lookup"><span data-stu-id="f7d13-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="f7d13-114">O comprimento máximo da cadeia de caracteres é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7d13-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="f7d13-115">O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres, mas comparações de nome de serviço sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f7d13-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="f7d13-116">Barras invertidas (/) e barras invertidas duplas ( \\ ) são caracteres de nome de serviço inválidos.</span><span class="sxs-lookup"><span data-stu-id="f7d13-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-117">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-118">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-118">Display name of the service.</span></span> <span data-ttu-id="f7d13-119">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f7d13-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="f7d13-120">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="f7d13-121">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f7d13-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="f7d13-122">Restrições: aceita o mesmo valor que o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="f7d13-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="f7d13-123">Exemplo: "atdisk".</span><span class="sxs-lookup"><span data-stu-id="f7d13-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-124">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-125">Caminho totalmente qualificado para o arquivo executável que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="f7d13-126">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="f7d13-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-127">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-128">Tipo de serviços fornecidos aos processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="f7d13-128">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="f7d13-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f7d13-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-130">Driver de kernel</span><span class="sxs-lookup"><span data-stu-id="f7d13-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="f7d13-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-132">Driver do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="f7d13-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="f7d13-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-134">Adaptador</span><span class="sxs-lookup"><span data-stu-id="f7d13-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="f7d13-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-136">Driver do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="f7d13-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="f7d13-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-138">Próprio processo</span><span class="sxs-lookup"><span data-stu-id="f7d13-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="f7d13-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-140">Processo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f7d13-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="f7d13-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-142">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="f7d13-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f7d13-143">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-144">Severidade do erro se o método **Create** falhar ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="f7d13-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="f7d13-145">Esse valor indica a ação realizada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="f7d13-145">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="f7d13-146">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f7d13-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="f7d13-147">0</span><span class="sxs-lookup"><span data-stu-id="f7d13-147">0</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-148">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f7d13-148">"Ignore"</span></span>

<span data-ttu-id="f7d13-149">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="f7d13-149">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-150">1</span><span class="sxs-lookup"><span data-stu-id="f7d13-150">1</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-151">"Normal"</span><span class="sxs-lookup"><span data-stu-id="f7d13-151">"Normal"</span></span>

<span data-ttu-id="f7d13-152">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="f7d13-152">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-153">2</span><span class="sxs-lookup"><span data-stu-id="f7d13-153">2</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-154">Muito</span><span class="sxs-lookup"><span data-stu-id="f7d13-154">"Severe"</span></span>

<span data-ttu-id="f7d13-155">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="f7d13-155">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-156">3</span><span class="sxs-lookup"><span data-stu-id="f7d13-156">3</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-157">Drasticamente</span><span class="sxs-lookup"><span data-stu-id="f7d13-157">"Critical"</span></span>

<span data-ttu-id="f7d13-158">O sistema tenta iniciar com uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="f7d13-158">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f7d13-159">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-159">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-160">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="f7d13-160">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="f7d13-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="f7d13-161"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="f7d13-162">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f7d13-162">Device driver started by the operating system loader.</span></span> <span data-ttu-id="f7d13-163">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="f7d13-163">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="f7d13-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**</span><span class="sxs-lookup"><span data-stu-id="f7d13-164"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="f7d13-165">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f7d13-165">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="f7d13-166">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="f7d13-166">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="f7d13-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**</span><span class="sxs-lookup"><span data-stu-id="f7d13-167"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="f7d13-168">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="f7d13-168">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="f7d13-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span><span class="sxs-lookup"><span data-stu-id="f7d13-169"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="f7d13-170">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d13-170">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f7d13-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="f7d13-171"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="f7d13-172">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="f7d13-172">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f7d13-173">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-173">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-174">Se **for true**, o serviço poderá criar ou se comunicar com as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f7d13-174">If **true**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-175">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-175">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-176">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="f7d13-176">Account name under which the service runs.</span></span> <span data-ttu-id="f7d13-177">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome do \\ usuário ou do formato UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="f7d13-177">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="f7d13-178">O processo de serviço é registrado usando uma dessas duas formas quando é executado.</span><span class="sxs-lookup"><span data-stu-id="f7d13-178">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="f7d13-179">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f7d13-179">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="f7d13-180">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f7d13-180">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="f7d13-181">Para um kernel ou drivers de nível de sistema, o *StartName* contém o nome do objeto de driver (ou seja, o sistema de \\ arquivos \\ rdr ou \\ \\ o driver XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7d13-181">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="f7d13-182">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-182">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="f7d13-183">Exemplo: administrador do DWDOM \\</span><span class="sxs-lookup"><span data-stu-id="f7d13-183">Example: DWDOM\\Admin</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-184">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-184">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-185">Senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="f7d13-185">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="f7d13-186">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="f7d13-186">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="f7d13-187">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="f7d13-187">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-188">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-188">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-189">Nome do grupo associado ao novo serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-189">Group name associated with the new service.</span></span> <span data-ttu-id="f7d13-190">Os grupos de ordem de carregamento estão contidos no registro e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f7d13-190">Load order groups are contained in the registry and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="f7d13-191">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="f7d13-191">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="f7d13-192">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="f7d13-192">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="f7d13-193">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="f7d13-193">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="f7d13-194">O registro tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="f7d13-194">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="f7d13-195">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="f7d13-195">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-196">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-196">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-197">Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-197">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="f7d13-198">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="f7d13-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="f7d13-199">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="f7d13-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="f7d13-200">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="f7d13-200">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f7d13-201">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-lo de um nome de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="f7d13-201">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="f7d13-202">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="f7d13-202">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="f7d13-203">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7d13-203">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d13-204">Uma matriz que contém os nomes de serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="f7d13-204">An array that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="f7d13-205">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="f7d13-205">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="f7d13-206">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="f7d13-206">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="f7d13-207">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="f7d13-207">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="f7d13-208">A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="f7d13-208">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d13-209">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7d13-209">Return value</span></span>

<span data-ttu-id="f7d13-210">Retorna um valor de 0 (zero) se o serviço foi criado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f7d13-210">Returns a value of 0 (zero) if the service was successfully created, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d13-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7d13-211">Requirements</span></span>



| <span data-ttu-id="f7d13-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7d13-212">Requirement</span></span> | <span data-ttu-id="f7d13-213">Valor</span><span class="sxs-lookup"><span data-stu-id="f7d13-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d13-214">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7d13-214">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d13-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7d13-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7d13-216">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7d13-216">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d13-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7d13-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7d13-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7d13-218">Namespace</span></span><br/>                | <span data-ttu-id="f7d13-219">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f7d13-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7d13-220">MOF</span><span class="sxs-lookup"><span data-stu-id="f7d13-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7d13-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7d13-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7d13-222">DLL</span><span class="sxs-lookup"><span data-stu-id="f7d13-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7d13-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7d13-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d13-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7d13-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7d13-225">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7d13-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f7d13-226">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="f7d13-226">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

