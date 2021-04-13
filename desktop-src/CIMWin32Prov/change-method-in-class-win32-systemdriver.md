---
description: Modifica um serviço do \_ SystemDriver Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Método Change da classe Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457085"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="5f328-103">Alterar o método da \_ classe systemdrive do Win32</span><span class="sxs-lookup"><span data-stu-id="5f328-103">Change method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="5f328-104">O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um serviço [**de \_ systemdrive do Win32**](win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="5f328-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_SystemDriver**](win32-systemdriver.md) service.</span></span> <span data-ttu-id="5f328-105">O parâmetro do grupo de [**\_ pedidos do Win32**](win32-loadordergroup.md) representa um agrupamento de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="5f328-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="5f328-106">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="5f328-106">The services must be initiated in the order specified by the Load Order Group as the services are dependent on each other.</span></span> <span data-ttu-id="5f328-107">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f328-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="5f328-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5f328-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5f328-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5f328-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f328-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f328-110">Syntax</span></span>


```mof
uint32 Change(
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



## <a name="parameters"></a><span data-ttu-id="5f328-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f328-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f328-112">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-113">O nome para exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="5f328-113">The display name of the service.</span></span> <span data-ttu-id="5f328-114">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f328-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="5f328-115">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="5f328-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="5f328-116">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5f328-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="5f328-117">Restrições: aceita o mesmo valor que o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="5f328-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="5f328-118">Exemplo: "atdisk"</span><span class="sxs-lookup"><span data-stu-id="5f328-118">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="5f328-119">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-120">O caminho totalmente qualificado para o arquivo executável que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="5f328-120">The fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="5f328-121">Exemplo: *\\ systemroot \\ System32 \\ drivers \\afd.sys*</span><span class="sxs-lookup"><span data-stu-id="5f328-121">Example: *\\SystemRoot\\System32\\drivers\\afd.sys*</span></span>

</dd> <dt>

<span data-ttu-id="5f328-122">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-123">Tipo de serviços fornecidos aos processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="5f328-123">Type of services provided to the processes that call them.</span></span>

<dt>

<span data-ttu-id="5f328-124">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="5f328-124">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-125">Driver de kernel</span><span class="sxs-lookup"><span data-stu-id="5f328-125">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="5f328-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="5f328-126">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-127">Driver do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="5f328-127">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="5f328-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="5f328-128">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-129">Adaptador</span><span class="sxs-lookup"><span data-stu-id="5f328-129">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="5f328-130">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="5f328-130">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-131">Driver do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="5f328-131">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="5f328-132">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="5f328-132">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-133">Próprio processo</span><span class="sxs-lookup"><span data-stu-id="5f328-133">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="5f328-134">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="5f328-134">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-135">Processo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="5f328-135">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="5f328-136">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="5f328-136">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="5f328-137">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="5f328-137">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5f328-138">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-139">A severidade do erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="5f328-139">The severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="5f328-140">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="5f328-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="5f328-141">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5f328-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="5f328-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** (0)</span><span class="sxs-lookup"><span data-stu-id="5f328-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5f328-143">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="5f328-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="5f328-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="5f328-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5f328-145">Normal.</span><span class="sxs-lookup"><span data-stu-id="5f328-145">Normal.</span></span> <span data-ttu-id="5f328-146">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="5f328-146">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="5f328-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severo** (2)</span><span class="sxs-lookup"><span data-stu-id="5f328-147"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5f328-148">O sistema é reiniciado com a última configuração válida.</span><span class="sxs-lookup"><span data-stu-id="5f328-148">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5f328-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="5f328-149"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5f328-150">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="5f328-150">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5f328-151">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-151">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-152">O modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="5f328-152">The start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="5f328-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial**</span><span class="sxs-lookup"><span data-stu-id="5f328-153"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="5f328-154">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5f328-154">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="5f328-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial**</span><span class="sxs-lookup"><span data-stu-id="5f328-155"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start**</span></span>


</dt> <dd>

<span data-ttu-id="5f328-156">Driver de dispositivo que o carregador do sistema operacional inicia.</span><span class="sxs-lookup"><span data-stu-id="5f328-156">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="5f328-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do sistema**</span><span class="sxs-lookup"><span data-stu-id="5f328-157"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**</span></span>


</dt> <dd>

<span data-ttu-id="5f328-158">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5f328-158">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="5f328-159">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="5f328-159">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="5f328-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático**</span><span class="sxs-lookup"><span data-stu-id="5f328-160"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start**</span></span>


</dt> <dd>

<span data-ttu-id="5f328-161">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="5f328-161">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="5f328-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda**</span><span class="sxs-lookup"><span data-stu-id="5f328-162"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start**</span></span>


</dt> <dd>

<span data-ttu-id="5f328-163">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="5f328-163">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5f328-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="5f328-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="5f328-165">Serviço que não pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="5f328-165">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5f328-166">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-166">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-167">Um valor que, se **for verdadeiro**, o serviço pode criar ou se comunicar com as janelas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5f328-167">A value that, if **True**, the service can create or communicate with the windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="5f328-168">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-168">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-169">O nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="5f328-169">The account name the service runs under.</span></span> <span data-ttu-id="5f328-170">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome_do_domínio \\ username ou. \\ Usu.</span><span class="sxs-lookup"><span data-stu-id="5f328-170">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="5f328-171">Quando ele é executado, o processo de serviço é registrado usando uma dessas duas formas.</span><span class="sxs-lookup"><span data-stu-id="5f328-171">When it runs, the service process is logged using one of these two forms.</span></span> <span data-ttu-id="5f328-172">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="5f328-172">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="5f328-173">Se uma cadeia de caracteres vazia for especificada, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="5f328-173">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="5f328-174">Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver, por exemplo, \\ \\ o FileSystem rdr ou \\ \\ o driver XNS), que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f328-174">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns), which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="5f328-175">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão que o sistema de e/s cria com base no nome do serviço, por exemplo, DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="5f328-175">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="5f328-176">Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="5f328-176">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="5f328-177">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-177">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-178">A senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="5f328-178">The password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="5f328-179">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="5f328-179">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="5f328-180">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="5f328-180">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="5f328-181">Ao alterar um serviço de um sistema local para uma rede, ou de uma rede para um sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f328-181">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="5f328-182">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-182">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-183">O nome do grupo ao qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="5f328-183">The group name that it is associated with.</span></span> <span data-ttu-id="5f328-184">Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5f328-184">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="5f328-185">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="5f328-185">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="5f328-186">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="5f328-186">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="5f328-187">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="5f328-187">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="5f328-188">O registro do sistema tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="5f328-188">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="5f328-189">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="5f328-189">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="5f328-190">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-190">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-191">A lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="5f328-191">The list of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="5f328-192">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5f328-192">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5f328-193">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="5f328-193">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5f328-194">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo WinSvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="5f328-194">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the WinSvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="5f328-195">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="5f328-195">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="5f328-196">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f328-196">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f328-197">A lista que contém os nomes dos serviços que devem iniciar antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="5f328-197">The list that contains the names of the services that must start before this service starts.</span></span> <span data-ttu-id="5f328-198">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5f328-198">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="5f328-199">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="5f328-199">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="5f328-200">A dependência de um serviço significa que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="5f328-200">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f328-201">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f328-201">Return value</span></span>

<span data-ttu-id="5f328-202">Retorna um valor de zero (0) se o serviço tiver sido modificado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="5f328-202">Returns a value of zero (0) if the service was successfully modified, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5f328-203">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="5f328-203">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-204">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5f328-204">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-205">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="5f328-205">**Access Denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-206">**Serviços dependentes em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="5f328-206">**Dependent Services Running** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-207">**Controle de serviço inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="5f328-207">**Invalid Service Control** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-208">O **serviço não pode aceitar o controle** (5)</span><span class="sxs-lookup"><span data-stu-id="5f328-208">**Service Cannot Accept Control** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-209">**Serviço não ativo** (6)</span><span class="sxs-lookup"><span data-stu-id="5f328-209">**Service Not Active** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-210">**Tempo limite da solicitação de serviço** (7)</span><span class="sxs-lookup"><span data-stu-id="5f328-210">**Service Request Timeout** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-211">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="5f328-211">**Unknown Failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-212">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="5f328-212">**Path Not Found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-213">**Serviço já em execução** (10)</span><span class="sxs-lookup"><span data-stu-id="5f328-213">**Service Already Running** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-214">**Banco de dados de serviço bloqueado** (11)</span><span class="sxs-lookup"><span data-stu-id="5f328-214">**Service Database Locked** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-215">**Dependência de serviço excluída** (12)</span><span class="sxs-lookup"><span data-stu-id="5f328-215">**Service Dependency Deleted** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-216">**Falha de dependência de serviço** (13)</span><span class="sxs-lookup"><span data-stu-id="5f328-216">**Service Dependency Failure** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-217">**Serviço desabilitado** (14)</span><span class="sxs-lookup"><span data-stu-id="5f328-217">**Service Disabled** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-218">**Falha no logon do serviço** (15)</span><span class="sxs-lookup"><span data-stu-id="5f328-218">**Service Logon Failed** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-219">**Serviço marcado para exclusão** (16)</span><span class="sxs-lookup"><span data-stu-id="5f328-219">**Service Marked For Deletion** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-220">**Serviço sem thread** (17)</span><span class="sxs-lookup"><span data-stu-id="5f328-220">**Service No Thread** (17)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-221">**Dependência circular de status** (18)</span><span class="sxs-lookup"><span data-stu-id="5f328-221">**Status Circular Dependency** (18)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-222">**Nome duplicado de status** (19)</span><span class="sxs-lookup"><span data-stu-id="5f328-222">**Status Duplicate Name** (19)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-223">**Nome inválido do status** (20)</span><span class="sxs-lookup"><span data-stu-id="5f328-223">**Status Invalid Name** (20)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-224">**Parâmetro de status inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="5f328-224">**Status Invalid Parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-225">**Conta de serviço inválida de status** (22)</span><span class="sxs-lookup"><span data-stu-id="5f328-225">**Status Invalid Service Account** (22)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-226">O **serviço de status existe** (23)</span><span class="sxs-lookup"><span data-stu-id="5f328-226">**Status Service Exists** (23)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-227">**Serviço já pausado** (24)</span><span class="sxs-lookup"><span data-stu-id="5f328-227">**Service Already Paused** (24)</span></span>
</dt> <dt>

<span data-ttu-id="5f328-228">**Outro** (25 4294967295)</span><span class="sxs-lookup"><span data-stu-id="5f328-228">**Other** (25 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5f328-229">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f328-229">Remarks</span></span>

<span data-ttu-id="5f328-230">Para alterar um serviço de um serviço de rede para o sistema local, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="5f328-230">To change a service from a network service to the local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="5f328-231">Para alterar um serviço de um serviço do sistema local para um serviço de rede, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="5f328-231">To change a service from a local system service to network service, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="5f328-232">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f328-232">Requirements</span></span>



| <span data-ttu-id="5f328-233">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f328-233">Requirement</span></span> | <span data-ttu-id="5f328-234">Valor</span><span class="sxs-lookup"><span data-stu-id="5f328-234">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f328-235">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f328-235">Minimum supported client</span></span><br/> | <span data-ttu-id="5f328-236">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f328-236">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f328-237">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f328-237">Minimum supported server</span></span><br/> | <span data-ttu-id="5f328-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f328-238">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f328-239">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f328-239">Namespace</span></span><br/>                | <span data-ttu-id="5f328-240">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5f328-240">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f328-241">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f328-241">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f328-242"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f328-242"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="5f328-243">MOF</span><span class="sxs-lookup"><span data-stu-id="5f328-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f328-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f328-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f328-245">DLL</span><span class="sxs-lookup"><span data-stu-id="5f328-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f328-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f328-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f328-247">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f328-247">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f328-248">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f328-248">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5f328-249">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="5f328-249">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

