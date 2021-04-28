---
title: Método Create da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método Create da classe Win32_Service (Serviços de Área de Trabalho Remota) – cria um novo serviço do sistema.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9daf877f56bb7e9bfcc349e4efb38635a9286a48
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090684"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="df8fd-106">Método Create da classe Win32_Service (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="df8fd-106">Create method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="df8fd-107">O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço do sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-107">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="df8fd-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="df8fd-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="df8fd-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="df8fd-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="df8fd-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df8fd-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="df8fd-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df8fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8fd-112">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-113">Nome do serviço a ser instalado para o método **Create** .</span><span class="sxs-lookup"><span data-stu-id="df8fd-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="df8fd-114">O comprimento máximo da cadeia de caracteres é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="df8fd-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="df8fd-115">O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres, mas comparações de nome de serviço sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="df8fd-115">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="df8fd-116">Barras invertidas (/) e barras invertidas duplas ( \) são caracteres de nome de serviço inválidos.</span><span class="sxs-lookup"><span data-stu-id="df8fd-116">Forward-slashes (/) and double back-slashes (\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-117">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-118">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-118">Display name of the service.</span></span> <span data-ttu-id="df8fd-119">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="df8fd-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="df8fd-120">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-120">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="df8fd-121">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="df8fd-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="df8fd-122">Restrições: aceita o mesmo valor que o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="df8fd-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="df8fd-123">Exemplo: "atdisk".</span><span class="sxs-lookup"><span data-stu-id="df8fd-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-124">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-125">Caminho totalmente qualificado para o arquivo executável que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="df8fd-126">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="df8fd-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-127">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-128">Tipo de serviços fornecidos para processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="df8fd-128">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="df8fd-129">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="df8fd-129">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-130">Driver de kernel</span><span class="sxs-lookup"><span data-stu-id="df8fd-130">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-131">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="df8fd-131">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-132">Driver do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="df8fd-132">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="df8fd-133">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-134">Adaptador</span><span class="sxs-lookup"><span data-stu-id="df8fd-134">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-135">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="df8fd-135">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-136">Driver do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="df8fd-136">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-137">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="df8fd-137">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-138">Próprio processo</span><span class="sxs-lookup"><span data-stu-id="df8fd-138">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-139">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="df8fd-139">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-140">Processo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="df8fd-140">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="df8fd-141">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-142">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="df8fd-142">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="df8fd-143">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-143">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-144">Severidade do erro se o método **Create** falhar ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="df8fd-144">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="df8fd-145">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="df8fd-145">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="df8fd-146">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-146">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="df8fd-147">0</span><span class="sxs-lookup"><span data-stu-id="df8fd-147">0</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-148">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-148">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-149">1</span><span class="sxs-lookup"><span data-stu-id="df8fd-149">1</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-150">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-150">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-151">2</span><span class="sxs-lookup"><span data-stu-id="df8fd-151">2</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-152">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="df8fd-152">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-153">3</span><span class="sxs-lookup"><span data-stu-id="df8fd-153">3</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-154">O sistema tenta iniciar com uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="df8fd-154">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="df8fd-155">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-155">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-156">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="df8fd-156">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="df8fd-157">Inicialização</span><span class="sxs-lookup"><span data-stu-id="df8fd-157">Boot</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-158">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="df8fd-158">Device driver started by the operating system loader.</span></span> <span data-ttu-id="df8fd-159">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="df8fd-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-160">Sistema</span><span class="sxs-lookup"><span data-stu-id="df8fd-160">System</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-161">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="df8fd-161">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="df8fd-162">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="df8fd-162">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-163">Automática</span><span class="sxs-lookup"><span data-stu-id="df8fd-163">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-164">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-164">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-165">Manual</span><span class="sxs-lookup"><span data-stu-id="df8fd-165">Manual</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-166">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="df8fd-166">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-167">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="df8fd-167">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-168">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-168">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="df8fd-169">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-169">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-170">Se **for true**, o serviço poderá criar ou se comunicar com o Windows na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="df8fd-170">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-171">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-171">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-172">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-172">Account name under which the service runs.</span></span> <span data-ttu-id="df8fd-173">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome do \\ usuário ou do formato UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="df8fd-173">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="df8fd-174">O processo de serviço é registrado usando uma dessas duas formas quando é executado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-174">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="df8fd-175">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-175">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="df8fd-176">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="df8fd-176">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="df8fd-177">Para um kernel ou drivers de nível de sistema, o *StartName* contém o nome do objeto de driver (ou seja, o sistema de \\ arquivos \\ rdr ou \\ \\ o driver XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df8fd-177">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="df8fd-178">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-178">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="df8fd-179">Exemplo: DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="df8fd-179">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-180">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-180">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-181">Senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="df8fd-181">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="df8fd-182">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="df8fd-182">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="df8fd-183">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="df8fd-183">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-184">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-184">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-185">Nome do grupo associado ao novo serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-185">Group name associated with the new service.</span></span> <span data-ttu-id="df8fd-186">Os grupos de ordem de carregamento estão contidos no registro e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="df8fd-186">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="df8fd-187">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="df8fd-187">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="df8fd-188">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="df8fd-188">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="df8fd-189">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="df8fd-189">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="df8fd-190">O registro tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="df8fd-190">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="df8fd-191">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="df8fd-191">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-192">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-192">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-193">Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-193">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="df8fd-194">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="df8fd-194">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="df8fd-195">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="df8fd-195">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="df8fd-196">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="df8fd-196">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="df8fd-197">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-lo de um nome de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="df8fd-197">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="df8fd-198">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="df8fd-198">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-199">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df8fd-199">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-200">Matriz que contém nomes de serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-200">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="df8fd-201">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="df8fd-201">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="df8fd-202">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="df8fd-202">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="df8fd-203">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="df8fd-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="df8fd-204">A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="df8fd-204">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8fd-205">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="df8fd-205">Return value</span></span>

<span data-ttu-id="df8fd-206">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="df8fd-206">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="df8fd-207">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="df8fd-207">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="df8fd-208">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="df8fd-208">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="df8fd-209">**0**</span><span class="sxs-lookup"><span data-stu-id="df8fd-209">**0**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-210">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="df8fd-210">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-211">**1**</span><span class="sxs-lookup"><span data-stu-id="df8fd-211">**1**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-212">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="df8fd-212">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-213">**2**</span><span class="sxs-lookup"><span data-stu-id="df8fd-213">**2**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-214">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="df8fd-214">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-215">**3**</span><span class="sxs-lookup"><span data-stu-id="df8fd-215">**3**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-216">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="df8fd-216">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-217">**4**</span><span class="sxs-lookup"><span data-stu-id="df8fd-217">**4**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-218">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-218">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-219">**5**</span><span class="sxs-lookup"><span data-stu-id="df8fd-219">**5**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-220">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço (propriedade **State** da classe [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) ) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="df8fd-220">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-221">**6**</span><span class="sxs-lookup"><span data-stu-id="df8fd-221">**6**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-222">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-223">**7**</span><span class="sxs-lookup"><span data-stu-id="df8fd-223">**7**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-224">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="df8fd-224">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-225">**8**</span><span class="sxs-lookup"><span data-stu-id="df8fd-225">**8**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-226">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-226">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-227">**9**</span><span class="sxs-lookup"><span data-stu-id="df8fd-227">**9**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-228">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-228">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-229">**10**</span><span class="sxs-lookup"><span data-stu-id="df8fd-229">**10**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-230">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="df8fd-230">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-231">**11**</span><span class="sxs-lookup"><span data-stu-id="df8fd-231">**11**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-232">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-232">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-233">**12**</span><span class="sxs-lookup"><span data-stu-id="df8fd-233">**12**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-234">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-234">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-235">**13**</span><span class="sxs-lookup"><span data-stu-id="df8fd-235">**13**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-236">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="df8fd-236">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-237">**14**</span><span class="sxs-lookup"><span data-stu-id="df8fd-237">**14**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-238">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-238">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-239">**15**</span><span class="sxs-lookup"><span data-stu-id="df8fd-239">**15**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-240">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-240">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-241">**16**</span><span class="sxs-lookup"><span data-stu-id="df8fd-241">**16**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-242">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-242">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-243">**17**</span><span class="sxs-lookup"><span data-stu-id="df8fd-243">**17**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-244">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="df8fd-244">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-245">**anos**</span><span class="sxs-lookup"><span data-stu-id="df8fd-245">**18**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-246">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="df8fd-246">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-247">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="df8fd-247">**19**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-248">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="df8fd-248">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-249">**20**</span><span class="sxs-lookup"><span data-stu-id="df8fd-249">**20**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-250">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="df8fd-250">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-251">**Abril**</span><span class="sxs-lookup"><span data-stu-id="df8fd-251">**21**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-252">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-252">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-253">**22**</span><span class="sxs-lookup"><span data-stu-id="df8fd-253">**22**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-254">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-254">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-255">**23**</span><span class="sxs-lookup"><span data-stu-id="df8fd-255">**23**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-256">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-256">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="df8fd-257">**24**</span><span class="sxs-lookup"><span data-stu-id="df8fd-257">**24**</span></span>
</dt> <dd>

<span data-ttu-id="df8fd-258">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="df8fd-258">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df8fd-259">Comentários</span><span class="sxs-lookup"><span data-stu-id="df8fd-259">Remarks</span></span>

<span data-ttu-id="df8fd-260">Os serviços geralmente são instalados de uma das duas maneiras: como parte da instalação do sistema operacional ou usando um programa de instalação fornecido pelo desenvolvedor do serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-260">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="df8fd-261">No entanto, alguns serviços, especialmente aqueles criados internamente, podem não ter um programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="df8fd-261">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="df8fd-262">Nessas instâncias, você pode usar o método **Create** para instalar serviços programaticamente.</span><span class="sxs-lookup"><span data-stu-id="df8fd-262">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="df8fd-263">Apesar do nome, o método Create não cria realmente um serviço; Ele simplesmente instala um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="df8fd-263">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="df8fd-264">Para usar esse comando, você precisa copiar o arquivo executável do serviço para um computador e, em seguida, usar **criar** para instalar o serviço.</span><span class="sxs-lookup"><span data-stu-id="df8fd-264">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="df8fd-265">O método **Create** é semelhante ao método [**Change**](win32-terminalservice-change.md) .</span><span class="sxs-lookup"><span data-stu-id="df8fd-265">The **Create** method is similar to the [**Change**](win32-terminalservice-change.md) method.</span></span> <span data-ttu-id="df8fd-266">Em ambos os casos, as propriedades do serviço são passadas como parâmetros para o método.</span><span class="sxs-lookup"><span data-stu-id="df8fd-266">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="df8fd-267">Assim como com os parâmetros usados com o método **Change** , a ordem na qual esses parâmetros são passados é muito importante.</span><span class="sxs-lookup"><span data-stu-id="df8fd-267">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="df8fd-268">O parâmetro *Loadordener* representa um agrupamento de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="df8fd-268">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="df8fd-269">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="df8fd-269">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="df8fd-270">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="df8fd-270">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8fd-271">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df8fd-271">Requirements</span></span>



| <span data-ttu-id="df8fd-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="df8fd-272">Requirement</span></span> | <span data-ttu-id="df8fd-273">Valor</span><span class="sxs-lookup"><span data-stu-id="df8fd-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df8fd-274">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df8fd-274">Minimum supported client</span></span><br/> | <span data-ttu-id="df8fd-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df8fd-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df8fd-276">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df8fd-276">Minimum supported server</span></span><br/> | <span data-ttu-id="df8fd-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df8fd-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df8fd-278">Namespace</span><span class="sxs-lookup"><span data-stu-id="df8fd-278">Namespace</span></span><br/>                | <span data-ttu-id="df8fd-279">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="df8fd-279">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="df8fd-280">MOF</span><span class="sxs-lookup"><span data-stu-id="df8fd-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df8fd-281"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df8fd-281"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="df8fd-282">DLL</span><span class="sxs-lookup"><span data-stu-id="df8fd-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df8fd-283"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df8fd-283"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df8fd-284">Consulte também</span><span class="sxs-lookup"><span data-stu-id="df8fd-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8fd-285">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="df8fd-285">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="df8fd-286">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="df8fd-286">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="df8fd-287">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="df8fd-287">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="df8fd-288">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="df8fd-288">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

