---
description: Modifica um serviço Win32 \_ .
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Método Change da classe Win32_Service (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501018"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a><span data-ttu-id="6389f-103">Método Change da classe Win32_Service (Mbnapi. h)</span><span class="sxs-lookup"><span data-stu-id="6389f-103">Change method of the Win32_Service class (Mbnapi.h)</span></span>

<span data-ttu-id="6389f-104">O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um [**\_ serviço Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="6389f-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="6389f-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6389f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6389f-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6389f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6389f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6389f-107">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a><span data-ttu-id="6389f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6389f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6389f-109">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-109">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-110">O nome para exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-110">The display name of the service.</span></span> <span data-ttu-id="6389f-111">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6389f-111">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="6389f-112">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-112">The name is case- preserved in the service control manager.</span></span> <span data-ttu-id="6389f-113">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6389f-113">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="6389f-114">Restrições: aceita o mesmo valor que a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="6389f-114">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="6389f-115">Exemplo, "atdisk".</span><span class="sxs-lookup"><span data-stu-id="6389f-115">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="6389f-116">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-116">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-117">O caminho totalmente qualificado para o arquivo executável que implementa o serviço, por exemplo, " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="6389f-117">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="6389f-118">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-118">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-119">O tipo de serviços fornecidos aos processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="6389f-119">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="6389f-120">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6389f-120">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-121">Driver de kernel</span><span class="sxs-lookup"><span data-stu-id="6389f-121">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="6389f-122">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="6389f-122">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-123">Driver do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="6389f-123">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="6389f-124">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="6389f-124">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-125">Adaptador</span><span class="sxs-lookup"><span data-stu-id="6389f-125">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="6389f-126">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="6389f-126">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-127">Driver do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="6389f-127">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="6389f-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="6389f-128">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-129">Próprio processo</span><span class="sxs-lookup"><span data-stu-id="6389f-129">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="6389f-130">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="6389f-130">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-131">Processo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="6389f-131">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="6389f-132">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="6389f-132">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="6389f-133">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="6389f-133">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6389f-134">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-134">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-135">Severidade do erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="6389f-135">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="6389f-136">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="6389f-136">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="6389f-137">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-137">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="6389f-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** (0)</span><span class="sxs-lookup"><span data-stu-id="6389f-138"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6389f-139">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="6389f-139">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="6389f-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="6389f-140"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6389f-141">Normal.</span><span class="sxs-lookup"><span data-stu-id="6389f-141">Normal.</span></span> <span data-ttu-id="6389f-142">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="6389f-142">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="6389f-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severo** (2)</span><span class="sxs-lookup"><span data-stu-id="6389f-143"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6389f-144">O sistema é reiniciado com a última configuração válida.</span><span class="sxs-lookup"><span data-stu-id="6389f-144">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6389f-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="6389f-145"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6389f-146">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="6389f-146">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6389f-147">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-147">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-148">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="6389f-148">Start mode of the Windows base service.</span></span> <span data-ttu-id="6389f-149">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="6389f-149">For more information, see the Remarks section.</span></span>

<dt>

<span data-ttu-id="6389f-150">Inicialização</span><span class="sxs-lookup"><span data-stu-id="6389f-150">Boot</span></span>
</dt> <dd>

<span data-ttu-id="6389f-151">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6389f-151">Device driver started by the operating system loader.</span></span> <span data-ttu-id="6389f-152">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="6389f-152">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-153">Sistema</span><span class="sxs-lookup"><span data-stu-id="6389f-153">System</span></span>
</dt> <dd>

<span data-ttu-id="6389f-154">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6389f-154">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="6389f-155">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="6389f-155">This value is valid only for driver services.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-156">Automática</span><span class="sxs-lookup"><span data-stu-id="6389f-156">Automatic</span></span>
</dt> <dd>

<span data-ttu-id="6389f-157">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-157">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-158">Manual</span><span class="sxs-lookup"><span data-stu-id="6389f-158">Manual</span></span>
</dt> <dd>

<span data-ttu-id="6389f-159">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="6389f-159">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-160">Desabilitado</span><span class="sxs-lookup"><span data-stu-id="6389f-160">Disabled</span></span>
</dt> <dd>

<span data-ttu-id="6389f-161">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="6389f-161">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6389f-162">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-162">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-163">Se **for true**, o serviço poderá criar ou se comunicar com uma janela na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6389f-163">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-164">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-164">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-165">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="6389f-165">Account name the service runs under.</span></span> <span data-ttu-id="6389f-166">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome_do_domínio \\ username ou. \\ Usu.</span><span class="sxs-lookup"><span data-stu-id="6389f-166">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="6389f-167">O processo de serviço será registrado usando uma dessas duas formas quando for executado.</span><span class="sxs-lookup"><span data-stu-id="6389f-167">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="6389f-168">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="6389f-168">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="6389f-169">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="6389f-169">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="6389f-170">Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver (ou seja, \\ FileSystem \\ rdr ou o \\ Driver \\ XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6389f-170">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="6389f-171">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço, por exemplo, "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="6389f-171">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="6389f-172">Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="6389f-172">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-173">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-173">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-174">Senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="6389f-174">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="6389f-175">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="6389f-175">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="6389f-176">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="6389f-176">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="6389f-177">Ao alterar um serviço de um sistema local para uma rede, ou de uma rede para um sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6389f-177">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="6389f-178">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-178">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-179">Nome do grupo ao qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="6389f-179">Group name that it is associated with.</span></span> <span data-ttu-id="6389f-180">Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6389f-180">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="6389f-181">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="6389f-181">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="6389f-182">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="6389f-182">For more information, see the Remarks section.</span></span>

<span data-ttu-id="6389f-183">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="6389f-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="6389f-184">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="6389f-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="6389f-185">O registro do sistema tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="6389f-185">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="6389f-186">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="6389f-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="6389f-187">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-188">Lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-188">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="6389f-189">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6389f-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="6389f-190">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="6389f-190">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="6389f-191">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador de grupo SC** (definido no arquivo Winsvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="6389f-191">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="6389f-192">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="6389f-192">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-193">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6389f-193">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6389f-194">Lista que contém os nomes dos serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-194">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="6389f-195">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6389f-195">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="6389f-196">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="6389f-196">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="6389f-197">A dependência em um serviço indica que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="6389f-197">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6389f-198">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6389f-198">Return value</span></span>

<span data-ttu-id="6389f-199">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="6389f-199">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="6389f-200">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6389f-200">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6389f-201">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6389f-201">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6389f-202">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="6389f-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-203">0</span><span class="sxs-lookup"><span data-stu-id="6389f-203">0</span></span>

<span data-ttu-id="6389f-204">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="6389f-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-205">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="6389f-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-206">1</span><span class="sxs-lookup"><span data-stu-id="6389f-206">1</span></span>

<span data-ttu-id="6389f-207">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="6389f-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-208">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="6389f-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-209">2</span><span class="sxs-lookup"><span data-stu-id="6389f-209">2</span></span>

<span data-ttu-id="6389f-210">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="6389f-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-211">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="6389f-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-212">3</span><span class="sxs-lookup"><span data-stu-id="6389f-212">3</span></span>

<span data-ttu-id="6389f-213">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="6389f-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-214">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="6389f-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-215">4</span><span class="sxs-lookup"><span data-stu-id="6389f-215">4</span></span>

<span data-ttu-id="6389f-216">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-217">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="6389f-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-218">5</span><span class="sxs-lookup"><span data-stu-id="6389f-218">5</span></span>

<span data-ttu-id="6389f-219">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="6389f-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-220">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="6389f-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-221">6</span><span class="sxs-lookup"><span data-stu-id="6389f-221">6</span></span>

<span data-ttu-id="6389f-222">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6389f-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-223">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="6389f-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-224">7</span><span class="sxs-lookup"><span data-stu-id="6389f-224">7</span></span>

<span data-ttu-id="6389f-225">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="6389f-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-226">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="6389f-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-227">8</span><span class="sxs-lookup"><span data-stu-id="6389f-227">8</span></span>

<span data-ttu-id="6389f-228">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-228">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-229">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="6389f-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-230">9</span><span class="sxs-lookup"><span data-stu-id="6389f-230">9</span></span>

<span data-ttu-id="6389f-231">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6389f-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-232">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="6389f-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-233">10</span><span class="sxs-lookup"><span data-stu-id="6389f-233">10</span></span>

<span data-ttu-id="6389f-234">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="6389f-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-235">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="6389f-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-236">11</span><span class="sxs-lookup"><span data-stu-id="6389f-236">11</span></span>

<span data-ttu-id="6389f-237">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6389f-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-238">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="6389f-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-239">12</span><span class="sxs-lookup"><span data-stu-id="6389f-239">12</span></span>

<span data-ttu-id="6389f-240">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-241">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="6389f-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-242">13</span><span class="sxs-lookup"><span data-stu-id="6389f-242">13</span></span>

<span data-ttu-id="6389f-243">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="6389f-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-244">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="6389f-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-245">14</span><span class="sxs-lookup"><span data-stu-id="6389f-245">14</span></span>

<span data-ttu-id="6389f-246">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-247">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="6389f-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-248">15</span><span class="sxs-lookup"><span data-stu-id="6389f-248">15</span></span>

<span data-ttu-id="6389f-249">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-250">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="6389f-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-251">16</span><span class="sxs-lookup"><span data-stu-id="6389f-251">16</span></span>

<span data-ttu-id="6389f-252">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-253">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="6389f-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-254">17</span><span class="sxs-lookup"><span data-stu-id="6389f-254">17</span></span>

<span data-ttu-id="6389f-255">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="6389f-255">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-256">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="6389f-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-257">18</span><span class="sxs-lookup"><span data-stu-id="6389f-257">18</span></span>

<span data-ttu-id="6389f-258">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="6389f-258">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-259">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="6389f-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-260">19</span><span class="sxs-lookup"><span data-stu-id="6389f-260">19</span></span>

<span data-ttu-id="6389f-261">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="6389f-261">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-262">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="6389f-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-263">20</span><span class="sxs-lookup"><span data-stu-id="6389f-263">20</span></span>

<span data-ttu-id="6389f-264">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="6389f-264">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-265">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="6389f-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-266">21</span><span class="sxs-lookup"><span data-stu-id="6389f-266">21</span></span>

<span data-ttu-id="6389f-267">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-268">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="6389f-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-269">22</span><span class="sxs-lookup"><span data-stu-id="6389f-269">22</span></span>

<span data-ttu-id="6389f-270">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-270">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-271">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="6389f-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-272">23</span><span class="sxs-lookup"><span data-stu-id="6389f-272">23</span></span>

<span data-ttu-id="6389f-273">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-274">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="6389f-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-275">24</span><span class="sxs-lookup"><span data-stu-id="6389f-275">24</span></span>

<span data-ttu-id="6389f-276">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="6389f-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="6389f-277">**Outras**</span><span class="sxs-lookup"><span data-stu-id="6389f-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="6389f-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="6389f-278">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6389f-279">Comentários</span><span class="sxs-lookup"><span data-stu-id="6389f-279">Remarks</span></span>

<span data-ttu-id="6389f-280">Quando um computador é iniciado, todos os serviços de inicialização automática também são iniciados.</span><span class="sxs-lookup"><span data-stu-id="6389f-280">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="6389f-281">Na ocasião, um desses serviços pode falhar ao iniciar junto com o computador.</span><span class="sxs-lookup"><span data-stu-id="6389f-281">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="6389f-282">Quando um serviço falha durante a inicialização do sistema, o computador executa uma ação com base no valor do código de controle de erro do serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-282">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="6389f-283">a maioria dos serviços é instalada usando o código de controle de erro normal.</span><span class="sxs-lookup"><span data-stu-id="6389f-283">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="6389f-284">Algumas das exceções, que são instaladas usando o código de erro ignorar, incluem:</span><span class="sxs-lookup"><span data-stu-id="6389f-284">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="6389f-285">Serviço de Replicação de Arquivos</span><span class="sxs-lookup"><span data-stu-id="6389f-285">File Replication Service</span></span>
-   <span data-ttu-id="6389f-286">Cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="6389f-286">Smart Card</span></span>
-   <span data-ttu-id="6389f-287">Logon Secundário</span><span class="sxs-lookup"><span data-stu-id="6389f-287">Secondary Logon</span></span>
-   <span data-ttu-id="6389f-288">WMI</span><span class="sxs-lookup"><span data-stu-id="6389f-288">WMI</span></span>

<span data-ttu-id="6389f-289">Para os serviços instalados usando o código de erro de ignorar, nenhuma notificação é dada ao usuário de que o serviço falhou.</span><span class="sxs-lookup"><span data-stu-id="6389f-289">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="6389f-290">Se preferir a notificação na tela informando que um serviço não pôde ser iniciado, você poderá usar o WMI para alterar o código de controle de erro.</span><span class="sxs-lookup"><span data-stu-id="6389f-290">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="6389f-291">Códigos de controle de erro se aplicam somente à inicialização do computador; os códigos de controle de erro não serão usados se você parar e, em seguida, tentar reiniciar um serviço depois que o computador estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="6389f-291">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="6389f-292">Na ocasião, talvez seja necessário alterar a conta sob a qual um determinado serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="6389f-292">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="6389f-293">Por exemplo, você pode executar um serviço em uma conta administrativa.</span><span class="sxs-lookup"><span data-stu-id="6389f-293">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="6389f-294">Como isso pode criar uma vulnerabilidade de segurança, você pode alternar o serviço para uma conta com menos privilégios.</span><span class="sxs-lookup"><span data-stu-id="6389f-294">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="6389f-295">Como alternativa, você pode ter serviços em execução em uma conta que está prestes a ser excluída, ou talvez queira garantir que, em todos os servidores, determinados serviços sejam executados em determinadas contas.</span><span class="sxs-lookup"><span data-stu-id="6389f-295">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="6389f-296">Você pode usar o método **Change** da classe [**de \_ serviço do Win32**](win32-service.md) para configurar os serviços para serem executados em uma conta de usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="6389f-296">You can use the **Change** method of the [**Win32\_Service**](win32-service.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="6389f-297">Ao selecionar uma conta, tenha em mente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6389f-297">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="6389f-298">A conta que está sendo usada como uma conta de serviço deve ter o direito de fazer logon como um serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-298">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="6389f-299">Esse direito pode ser concedido usando Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="6389f-299">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="6389f-300">A conta que está sendo usada como uma conta de serviço não deve ser membro de um grupo local, de domínio ou de administradores de empresa.</span><span class="sxs-lookup"><span data-stu-id="6389f-300">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="6389f-301">Cada instância de um serviço deve ser executada em uma conta de usuário exclusiva.</span><span class="sxs-lookup"><span data-stu-id="6389f-301">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="6389f-302">Isso fornece segurança adicional e habilita a auditoria de instâncias de serviço individuais.</span><span class="sxs-lookup"><span data-stu-id="6389f-302">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="6389f-303">Se o serviço for interativo, o serviço deverá ser executado na conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="6389f-303">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="6389f-304">O LocalSystem é necessário porque apenas uma estação de janela (WinSta0) pode ser visível e interativa por vez.</span><span class="sxs-lookup"><span data-stu-id="6389f-304">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="6389f-305">Se um serviço for executado em uma conta diferente de LocalSystem, ele será executado na estação de janela padrão Service-0x03E7 $ \\ , que é uma janela invisível.</span><span class="sxs-lookup"><span data-stu-id="6389f-305">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="6389f-306">Os serviços em execução nesta estação de janela não podem receber entrada ou exibir a saída.</span><span class="sxs-lookup"><span data-stu-id="6389f-306">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="6389f-307">Quando você atribui uma conta a um serviço, o SCM requer a senha correta para essa conta antes de fazer a atribuição.</span><span class="sxs-lookup"><span data-stu-id="6389f-307">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="6389f-308">Se você fornecer uma senha incorreta, o SCM rejeitará a conta.</span><span class="sxs-lookup"><span data-stu-id="6389f-308">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="6389f-309">Se você configurar uma conta de serviço usando a conta LocalSystem, LocalService ou NetworkService, não será necessário fornecer uma senha de conta, pois essas contas não têm senhas.</span><span class="sxs-lookup"><span data-stu-id="6389f-309">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="6389f-310">O SCM armazena a senha da conta no banco de dados de serviços.</span><span class="sxs-lookup"><span data-stu-id="6389f-310">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="6389f-311">No entanto, depois que a senha é atribuída, o SCM não garante que a senha armazenada no banco de dados de serviços e a senha atribuída à conta de usuário no Active Directory continuem a corresponder.</span><span class="sxs-lookup"><span data-stu-id="6389f-311">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="6389f-312">Consequentemente, uma situação semelhante à seguinte pode ocorrer:</span><span class="sxs-lookup"><span data-stu-id="6389f-312">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="6389f-313">Você configura um serviço para ser executado em uma conta de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="6389f-313">You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="6389f-314">O serviço é iniciado sob essa conta usando a senha da conta atual.</span><span class="sxs-lookup"><span data-stu-id="6389f-314">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="6389f-315">Você altera a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="6389f-315">You change the password for the user account.</span></span>
-   <span data-ttu-id="6389f-316">O serviço continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="6389f-316">The service continues to run.</span></span> <span data-ttu-id="6389f-317">No entanto, se o serviço for interrompido, você não poderá reiniciá-lo porque o SCM continua a usar a senha antiga e inválida.</span><span class="sxs-lookup"><span data-stu-id="6389f-317">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="6389f-318">Alterar a senha em Active Directory não altera a senha armazenada no banco de dados de serviços.</span><span class="sxs-lookup"><span data-stu-id="6389f-318">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="6389f-319">Se você executar serviços em contas de usuário regulares, precisará atualizar essas senhas de serviço sempre que a senha da conta de usuário for alterada.</span><span class="sxs-lookup"><span data-stu-id="6389f-319">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="6389f-320">Isso pode ser particularmente demorado se você não tiver certeza de quais serviços estão sendo executados nessa conta ou quais computadores têm serviços em execução nessa conta.</span><span class="sxs-lookup"><span data-stu-id="6389f-320">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="6389f-321">Felizmente, você pode usar o WMI para verificar as contas de serviço em todos os seus computadores e, se necessário, alterar a senha da conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="6389f-321">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="6389f-322">O parâmetro do [**\_ Sqlorder OrderGroup do Win32**](win32-loadordergroup.md) representa um grupo de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="6389f-322">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="6389f-323">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="6389f-323">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="6389f-324">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="6389f-324">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="6389f-325">Para alterar um serviço de um serviço de rede para um sistema local, os parâmetros *StartName* e *StartPassword* devem ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6389f-325">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="6389f-326">Para alterar um serviço de um serviço do sistema local para uma rede, os parâmetros *StartName* e *StartPassword* devem ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="6389f-326">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="6389f-327">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6389f-327">Examples</span></span>

<span data-ttu-id="6389f-328">O VBScript a seguir altera a conta de serviço para que os serviços sejam executados em uma conta de usuário especificada para LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="6389f-328">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="6389f-329">O VBScript a seguir altera a senha da conta de serviço para todos os scripts em execução em netsvc</span><span class="sxs-lookup"><span data-stu-id="6389f-329">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="6389f-330">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6389f-330">Requirements</span></span>



| <span data-ttu-id="6389f-331">Requisito</span><span class="sxs-lookup"><span data-stu-id="6389f-331">Requirement</span></span> | <span data-ttu-id="6389f-332">Valor</span><span class="sxs-lookup"><span data-stu-id="6389f-332">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6389f-333">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6389f-333">Minimum supported client</span></span><br/> | <span data-ttu-id="6389f-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6389f-334">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6389f-335">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6389f-335">Minimum supported server</span></span><br/> | <span data-ttu-id="6389f-336">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6389f-336">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6389f-337">Namespace</span><span class="sxs-lookup"><span data-stu-id="6389f-337">Namespace</span></span><br/>                | <span data-ttu-id="6389f-338">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6389f-338">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6389f-339">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6389f-339">Header</span></span><br/>                   | <dl> <span data-ttu-id="6389f-340"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6389f-340"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="6389f-341">MOF</span><span class="sxs-lookup"><span data-stu-id="6389f-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6389f-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6389f-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6389f-343">DLL</span><span class="sxs-lookup"><span data-stu-id="6389f-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6389f-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6389f-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6389f-345">Confira também</span><span class="sxs-lookup"><span data-stu-id="6389f-345">See also</span></span>

<dl> <dt>

<span data-ttu-id="6389f-346">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6389f-346">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6389f-347">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="6389f-347">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="6389f-348">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="6389f-348">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

