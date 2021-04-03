---
description: Cria um novo serviço do sistema.
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: Método Create da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f23bc2a5c49a85a20765172d4c5d361a8d18316
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646534"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="90454-103">Método Create da classe Win32_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="90454-103">Create method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="90454-104">O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço do sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new system service.</span></span>

<span data-ttu-id="90454-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="90454-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="90454-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="90454-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="90454-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90454-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="90454-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90454-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90454-109">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="90454-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-110">Nome do serviço a ser instalado para o método **Create** .</span><span class="sxs-lookup"><span data-stu-id="90454-110">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="90454-111">O comprimento máximo da cadeia de caracteres é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="90454-111">The maximum string length is 256 characters.</span></span> <span data-ttu-id="90454-112">O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres, mas comparações de nome de serviço sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="90454-112">The Service Control Manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="90454-113">Barras invertidas (/) e barras invertidas duplas ( \\ ) são caracteres de nome de serviço inválidos.</span><span class="sxs-lookup"><span data-stu-id="90454-113">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="90454-114">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-114">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-115">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-115">Display name of the service.</span></span> <span data-ttu-id="90454-116">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="90454-116">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="90454-117">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="90454-118">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="90454-118">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="90454-119">Restrições: aceita o mesmo valor que o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="90454-119">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="90454-120">Exemplo: "atdisk".</span><span class="sxs-lookup"><span data-stu-id="90454-120">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="90454-121">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-121">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-122">Caminho totalmente qualificado para o arquivo executável que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-122">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="90454-123">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="90454-123">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="90454-124">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-124">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-125">Tipo de serviços fornecidos para processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="90454-125">Type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="90454-126">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="90454-126">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="90454-127">Driver de kernel</span><span class="sxs-lookup"><span data-stu-id="90454-127">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="90454-128">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="90454-128">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="90454-129">Driver do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="90454-129">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="90454-130">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="90454-130">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="90454-131">Adaptador</span><span class="sxs-lookup"><span data-stu-id="90454-131">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="90454-132">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="90454-132">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="90454-133">Driver do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="90454-133">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="90454-134">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="90454-134">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="90454-135">Próprio processo</span><span class="sxs-lookup"><span data-stu-id="90454-135">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="90454-136">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="90454-136">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="90454-137">Processo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="90454-137">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="90454-138">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="90454-138">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="90454-139">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="90454-139">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="90454-140">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-140">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-141">Severidade do erro se o método **Create** falhar ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="90454-141">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="90454-142">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="90454-142">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="90454-143">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-143">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="90454-144">0</span><span class="sxs-lookup"><span data-stu-id="90454-144">0</span></span>
</dt> <dd>

<span data-ttu-id="90454-145">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="90454-145">User is not notified.</span></span>

</dd> <dt>

<span data-ttu-id="90454-146">1</span><span class="sxs-lookup"><span data-stu-id="90454-146">1</span></span>
</dt> <dd>

<span data-ttu-id="90454-147">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="90454-147">User is notified.</span></span>

</dd> <dt>

<span data-ttu-id="90454-148">2</span><span class="sxs-lookup"><span data-stu-id="90454-148">2</span></span>
</dt> <dd>

<span data-ttu-id="90454-149">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="90454-149">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span data-ttu-id="90454-150">3</span><span class="sxs-lookup"><span data-stu-id="90454-150">3</span></span>
</dt> <dd>

<span data-ttu-id="90454-151">O sistema tenta iniciar com uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="90454-151">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="90454-152">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-152">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-153">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="90454-153">Start mode of the Windows base service.</span></span>

<dt>

<span data-ttu-id="90454-154">Inicialização</span><span class="sxs-lookup"><span data-stu-id="90454-154">Boot</span></span>
</dt> <dd>

<span data-ttu-id="90454-155">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="90454-155">Device driver started by the operating system loader.</span></span> <span data-ttu-id="90454-156">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="90454-156">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="90454-157">Sistema</span><span class="sxs-lookup"><span data-stu-id="90454-157">System</span></span>
</dt> <dd>

<span data-ttu-id="90454-158">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="90454-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="90454-159">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="90454-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="90454-160">Automática</span><span class="sxs-lookup"><span data-stu-id="90454-160">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="90454-161">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-161">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="90454-162">Manual</span><span class="sxs-lookup"><span data-stu-id="90454-162">Manual</span></span>
</dt> <dd>

<span data-ttu-id="90454-163">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="90454-163">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="90454-164">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="90454-164">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="90454-165">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="90454-165">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="90454-166">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-167">Se **for true**, o serviço poderá criar ou se comunicar com o Windows na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="90454-167">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="90454-168">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-169">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="90454-169">Account name under which the service runs.</span></span> <span data-ttu-id="90454-170">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome do \\ usuário ou do formato UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="90454-170">Depending on the service type, the account name may be in the form of DomainName\\Username or User Principal Name (UPN) format (Username@DomainName).</span></span> <span data-ttu-id="90454-171">O processo de serviço é registrado usando uma dessas duas formas quando é executado.</span><span class="sxs-lookup"><span data-stu-id="90454-171">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="90454-172">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="90454-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="90454-173">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="90454-173">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="90454-174">Para um kernel ou drivers de nível de sistema, o *StartName* contém o nome do objeto de driver (ou seja, o sistema de \\ arquivos \\ rdr ou \\ \\ o driver XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90454-174">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="90454-175">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-175">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="90454-176">Exemplo: DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="90454-176">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="90454-177">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-178">Senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="90454-178">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="90454-179">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="90454-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="90454-180">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="90454-180">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="90454-181">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-181">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-182">Nome do grupo associado ao novo serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-182">Group name associated with the new service.</span></span> <span data-ttu-id="90454-183">Os grupos de ordem de carregamento estão contidos no registro e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="90454-183">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="90454-184">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="90454-184">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="90454-185">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="90454-185">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="90454-186">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="90454-186">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="90454-187">O registro tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="90454-187">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="90454-188">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="90454-188">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="90454-189">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-189">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-190">Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-190">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="90454-191">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="90454-191">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="90454-192">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="90454-192">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="90454-193">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="90454-193">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="90454-194">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-lo de um nome de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="90454-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="90454-195">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="90454-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="90454-196">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90454-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90454-197">Matriz que contém nomes de serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-197">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="90454-198">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="90454-198">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="90454-199">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="90454-199">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="90454-200">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="90454-200">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="90454-201">A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="90454-201">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90454-202">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90454-202">Return value</span></span>

<span data-ttu-id="90454-203">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="90454-203">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="90454-204">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="90454-204">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="90454-205">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="90454-205">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="90454-206">**0**</span><span class="sxs-lookup"><span data-stu-id="90454-206">**0**</span></span>
</dt> <dd>

<span data-ttu-id="90454-207">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="90454-207">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="90454-208">**1**</span><span class="sxs-lookup"><span data-stu-id="90454-208">**1**</span></span>
</dt> <dd>

<span data-ttu-id="90454-209">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="90454-209">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="90454-210">**2**</span><span class="sxs-lookup"><span data-stu-id="90454-210">**2**</span></span>
</dt> <dd>

<span data-ttu-id="90454-211">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="90454-211">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="90454-212">**3**</span><span class="sxs-lookup"><span data-stu-id="90454-212">**3**</span></span>
</dt> <dd>

<span data-ttu-id="90454-213">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="90454-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="90454-214">**4**</span><span class="sxs-lookup"><span data-stu-id="90454-214">**4**</span></span>
</dt> <dd>

<span data-ttu-id="90454-215">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-215">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="90454-216">**5**</span><span class="sxs-lookup"><span data-stu-id="90454-216">**5**</span></span>
</dt> <dd>

<span data-ttu-id="90454-217">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço (propriedade **State** da classe [**Win32 \_ BaseService**](win32-baseservice.md) ) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="90454-217">The requested control code cannot be sent to the service because the state of the service (**State** property of the [**Win32\_BaseService**](win32-baseservice.md) class) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="90454-218">**6**</span><span class="sxs-lookup"><span data-stu-id="90454-218">**6**</span></span>
</dt> <dd>

<span data-ttu-id="90454-219">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="90454-219">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="90454-220">**7**</span><span class="sxs-lookup"><span data-stu-id="90454-220">**7**</span></span>
</dt> <dd>

<span data-ttu-id="90454-221">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="90454-221">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="90454-222">**8**</span><span class="sxs-lookup"><span data-stu-id="90454-222">**8**</span></span>
</dt> <dd>

<span data-ttu-id="90454-223">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-223">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="90454-224">**9**</span><span class="sxs-lookup"><span data-stu-id="90454-224">**9**</span></span>
</dt> <dd>

<span data-ttu-id="90454-225">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="90454-225">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="90454-226">**10**</span><span class="sxs-lookup"><span data-stu-id="90454-226">**10**</span></span>
</dt> <dd>

<span data-ttu-id="90454-227">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="90454-227">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="90454-228">**11**</span><span class="sxs-lookup"><span data-stu-id="90454-228">**11**</span></span>
</dt> <dd>

<span data-ttu-id="90454-229">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="90454-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="90454-230">**12**</span><span class="sxs-lookup"><span data-stu-id="90454-230">**12**</span></span>
</dt> <dd>

<span data-ttu-id="90454-231">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-231">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="90454-232">**13**</span><span class="sxs-lookup"><span data-stu-id="90454-232">**13**</span></span>
</dt> <dd>

<span data-ttu-id="90454-233">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="90454-233">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="90454-234">**14**</span><span class="sxs-lookup"><span data-stu-id="90454-234">**14**</span></span>
</dt> <dd>

<span data-ttu-id="90454-235">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-235">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="90454-236">**15**</span><span class="sxs-lookup"><span data-stu-id="90454-236">**15**</span></span>
</dt> <dd>

<span data-ttu-id="90454-237">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-237">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="90454-238">**16**</span><span class="sxs-lookup"><span data-stu-id="90454-238">**16**</span></span>
</dt> <dd>

<span data-ttu-id="90454-239">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-239">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="90454-240">**17**</span><span class="sxs-lookup"><span data-stu-id="90454-240">**17**</span></span>
</dt> <dd>

<span data-ttu-id="90454-241">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="90454-241">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="90454-242">**anos**</span><span class="sxs-lookup"><span data-stu-id="90454-242">**18**</span></span>
</dt> <dd>

<span data-ttu-id="90454-243">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="90454-243">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="90454-244">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="90454-244">**19**</span></span>
</dt> <dd>

<span data-ttu-id="90454-245">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="90454-245">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="90454-246">**20**</span><span class="sxs-lookup"><span data-stu-id="90454-246">**20**</span></span>
</dt> <dd>

<span data-ttu-id="90454-247">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="90454-247">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="90454-248">**Abril**</span><span class="sxs-lookup"><span data-stu-id="90454-248">**21**</span></span>
</dt> <dd>

<span data-ttu-id="90454-249">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-249">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="90454-250">**22**</span><span class="sxs-lookup"><span data-stu-id="90454-250">**22**</span></span>
</dt> <dd>

<span data-ttu-id="90454-251">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-251">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="90454-252">**23**</span><span class="sxs-lookup"><span data-stu-id="90454-252">**23**</span></span>
</dt> <dd>

<span data-ttu-id="90454-253">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-253">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="90454-254">**24**</span><span class="sxs-lookup"><span data-stu-id="90454-254">**24**</span></span>
</dt> <dd>

<span data-ttu-id="90454-255">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="90454-255">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90454-256">Comentários</span><span class="sxs-lookup"><span data-stu-id="90454-256">Remarks</span></span>

<span data-ttu-id="90454-257">Os serviços geralmente são instalados de uma das duas maneiras: como parte da instalação do sistema operacional ou usando um programa de instalação fornecido pelo desenvolvedor do serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-257">Services are generally installed in one of two ways: either as a part of the operating system installation or by using an installation program provided by the service developer.</span></span> <span data-ttu-id="90454-258">No entanto, alguns serviços, especialmente aqueles criados internamente, podem não ter um programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="90454-258">However, some services, particularly those created in-house, might not have an installation program.</span></span> <span data-ttu-id="90454-259">Nessas instâncias, você pode usar o método **Create** para instalar serviços programaticamente.</span><span class="sxs-lookup"><span data-stu-id="90454-259">In those instances, you can use the **Create** method to programmatically install services.</span></span>

<span data-ttu-id="90454-260">Apesar do nome, o método Create não cria realmente um serviço; Ele simplesmente instala um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="90454-260">Despite the name, the Create method does not actually create a service; it merely installs an existing service.</span></span> <span data-ttu-id="90454-261">Para usar esse comando, você precisa copiar o arquivo executável do serviço para um computador e, em seguida, usar **criar** para instalar o serviço.</span><span class="sxs-lookup"><span data-stu-id="90454-261">To use this command, you need to copy the service executable file to a computer and then use **Create** to install the service.</span></span>

<span data-ttu-id="90454-262">O método **Create** é semelhante ao método [**Change**](change-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="90454-262">The **Create** method is similar to the [**Change**](change-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="90454-263">Em ambos os casos, as propriedades do serviço são passadas como parâmetros para o método.</span><span class="sxs-lookup"><span data-stu-id="90454-263">In both cases, the properties of the service are passed as parameters to the method.</span></span> <span data-ttu-id="90454-264">Assim como com os parâmetros usados com o método **Change** , a ordem na qual esses parâmetros são passados é muito importante.</span><span class="sxs-lookup"><span data-stu-id="90454-264">As with the parameters used with the **Change** method, the order in which these parameters are passed is very important.</span></span>

<span data-ttu-id="90454-265">O parâmetro *Loadordener* representa um agrupamento de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="90454-265">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="90454-266">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="90454-266">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="90454-267">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="90454-267">These dependent services require the presence of the antecedent services to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="90454-268">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90454-268">Examples</span></span>

<span data-ttu-id="90454-269">O VBScript a seguir instala um serviço chamado DbService</span><span class="sxs-lookup"><span data-stu-id="90454-269">The following VBScript installs a service named DbService</span></span>


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a><span data-ttu-id="90454-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90454-270">Requirements</span></span>



| <span data-ttu-id="90454-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="90454-271">Requirement</span></span> | <span data-ttu-id="90454-272">Valor</span><span class="sxs-lookup"><span data-stu-id="90454-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90454-273">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90454-273">Minimum supported client</span></span><br/> | <span data-ttu-id="90454-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90454-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90454-275">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90454-275">Minimum supported server</span></span><br/> | <span data-ttu-id="90454-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90454-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90454-277">Namespace</span><span class="sxs-lookup"><span data-stu-id="90454-277">Namespace</span></span><br/>                | <span data-ttu-id="90454-278">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="90454-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90454-279">MOF</span><span class="sxs-lookup"><span data-stu-id="90454-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90454-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90454-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90454-281">DLL</span><span class="sxs-lookup"><span data-stu-id="90454-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90454-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90454-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90454-283">Confira também</span><span class="sxs-lookup"><span data-stu-id="90454-283">See also</span></span>

<dl> <dt>

<span data-ttu-id="90454-284">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90454-284">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="90454-285">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="90454-285">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="90454-286">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="90454-286">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

