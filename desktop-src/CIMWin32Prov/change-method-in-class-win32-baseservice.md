---
description: Modifica um objeto de serviço derivado do Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Método Change da classe Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089410"
---
# <a name="change-method-of-the-win32_baseservice-class"></a><span data-ttu-id="c97ff-103">Método Change da classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="c97ff-103">Change method of the Win32\_BaseService class</span></span>

<span data-ttu-id="c97ff-104">O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um objeto de serviço derivado de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="c97ff-104">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span> <span data-ttu-id="c97ff-105">O parâmetro do [**\_ Sqlorder OrderGroup do Win32**](win32-loadordergroup.md) representa um grupo de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="c97ff-105">The [**Win32\_LoadOrderGroup**](win32-loadordergroup.md) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="c97ff-106">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="c97ff-106">The services must be initiated in the order specified by the Load Order Group, because the services depend on each other.</span></span> <span data-ttu-id="c97ff-107">Esses serviços dependentes exigem que os serviços antecedentes funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="c97ff-107">These dependent services require antecedent services to function correctly.</span></span>

<span data-ttu-id="c97ff-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c97ff-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c97ff-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c97ff-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c97ff-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c97ff-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c97ff-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c97ff-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97ff-112">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-113">O nome de exibição de um serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-113">The display name for a service.</span></span> <span data-ttu-id="c97ff-114">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c97ff-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="c97ff-115">O nome é o caso preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-115">The name is case preserved in the service control manager.</span></span> <span data-ttu-id="c97ff-116">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c97ff-116">*DisplayName* comparisons are always case insensitive.</span></span>

<span data-ttu-id="c97ff-117">Restrições: aceita o mesmo valor que o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="c97ff-117">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="c97ff-118">Exemplo: "atdisk".</span><span class="sxs-lookup"><span data-stu-id="c97ff-118">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-119">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-120">O caminho totalmente qualificado para o arquivo executável que implementa um serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-120">The fully qualified path to the executable file that implements a service.</span></span>

<span data-ttu-id="c97ff-121">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="c97ff-121">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-122">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-122">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-123">Tipo de serviços fornecidos para processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="c97ff-123">Type of services provided to processes that call them.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="c97ff-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver de kernel** (1)</span><span class="sxs-lookup"><span data-stu-id="c97ff-124"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="c97ff-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver do sistema de arquivos** (2)</span><span class="sxs-lookup"><span data-stu-id="c97ff-125"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="c97ff-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)</span><span class="sxs-lookup"><span data-stu-id="c97ff-126"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="c97ff-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver do reconhecedor** (8)</span><span class="sxs-lookup"><span data-stu-id="c97ff-127"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="c97ff-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Próprio processo** (16)</span><span class="sxs-lookup"><span data-stu-id="c97ff-128"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="c97ff-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo de compartilhamento** (32)</span><span class="sxs-lookup"><span data-stu-id="c97ff-129"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c97ff-130">(256)</span><span class="sxs-lookup"><span data-stu-id="c97ff-130">(256)</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-131">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="c97ff-131">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c97ff-132">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-132">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-133">Severidade de um erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="c97ff-133">Severity of an error if this service does not start during startup.</span></span> <span data-ttu-id="c97ff-134">O valor indica a ação que o programa de inicialização executará se ocorrer uma falha.</span><span class="sxs-lookup"><span data-stu-id="c97ff-134">The value indicates the action that the startup program takes if failure occurs.</span></span> <span data-ttu-id="c97ff-135">O sistema registra todos os erros.</span><span class="sxs-lookup"><span data-stu-id="c97ff-135">The system logs all errors.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="c97ff-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** (0)</span><span class="sxs-lookup"><span data-stu-id="c97ff-136"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-137">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-137">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="c97ff-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="c97ff-138"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-139">Normal.</span><span class="sxs-lookup"><span data-stu-id="c97ff-139">Normal.</span></span> <span data-ttu-id="c97ff-140">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-140">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="c97ff-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severo** (2)</span><span class="sxs-lookup"><span data-stu-id="c97ff-141"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-142">O sistema é reiniciado com a última configuração válida.</span><span class="sxs-lookup"><span data-stu-id="c97ff-142">System is restarted with the last good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="c97ff-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="c97ff-143"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-144">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="c97ff-144">System attempts to restart with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c97ff-145">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-145">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-146">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="c97ff-146">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="c97ff-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="c97ff-147"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-148">Driver de dispositivo que o carregador do sistema operacional inicia.</span><span class="sxs-lookup"><span data-stu-id="c97ff-148">Device driver that the operating system loader starts.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="c97ff-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="c97ff-149"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-150">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c97ff-150">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c97ff-151">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="c97ff-151">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="c97ff-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="c97ff-152"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-153">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-153">Service to start automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="c97ff-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")</span><span class="sxs-lookup"><span data-stu-id="c97ff-154"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-155">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c97ff-155">Service to start by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c97ff-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="c97ff-156"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="c97ff-157">Serviço que não pode ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-157">Service that cannot be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c97ff-158">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-158">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-159">Se **for true**, o serviço poderá criar ou se comunicar com uma janela na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c97ff-159">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-160">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-160">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-161">Nome da conta sob a qual o serviço é executado, o que depende do tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-161">Account name that the service runs under, which depends on the service type.</span></span> <span data-ttu-id="c97ff-162">O nome da conta pode estar na forma de DomainName \\ username ou. \\ Usu.</span><span class="sxs-lookup"><span data-stu-id="c97ff-162">The account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="c97ff-163">Quando é executado, o processo de serviço é registrado usando uma das duas formas anteriores.</span><span class="sxs-lookup"><span data-stu-id="c97ff-163">When it runs, the service process is logged by using one of the previous two forms.</span></span> <span data-ttu-id="c97ff-164">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-164">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="c97ff-165">Se uma cadeia de caracteres vazia for especificada, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="c97ff-165">If an empty string is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="c97ff-166">Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver, por exemplo, \\ \\ o FileSystem rdr ou \\ \\ o driver XNS, que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c97ff-166">For kernel or system-level drivers, *StartName* contains the driver object name, for example, \\FileSystem\\Rdr or \\Driver\\Xns, which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="c97ff-167">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão que o sistema de e/s cria com base no nome do serviço, por exemplo, DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="c97ff-167">If **NULL** is specified, the driver runs with a default object name that the I/O system creates based on the service name, for example, DWDOM\\Admin.</span></span>

<span data-ttu-id="c97ff-168">Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="c97ff-168">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-169">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-169">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-170">Senha para o nome da conta que o parâmetro *StartName* especifica.</span><span class="sxs-lookup"><span data-stu-id="c97ff-170">Password to the account name that the *StartName* parameter specifies.</span></span> <span data-ttu-id="c97ff-171">Especifique **NULL** quando você não alterar a senha.</span><span class="sxs-lookup"><span data-stu-id="c97ff-171">Specify **NULL** when you do not change the password.</span></span> <span data-ttu-id="c97ff-172">Especifique uma cadeia de caracteres vazia se o serviço não tiver uma senha.</span><span class="sxs-lookup"><span data-stu-id="c97ff-172">Specify an empty string if the service does not have a password.</span></span>

> [!Note]  
> <span data-ttu-id="c97ff-173">Quando você altera um serviço do sistema local para a rede ou da rede para o sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c97ff-173">When you change a service from local system to network or from network to local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="c97ff-174">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-174">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-175">Nome do grupo ao qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-175">Group name that it is associated with.</span></span> <span data-ttu-id="c97ff-176">Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência em que os serviços são carregados em um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c97ff-176">Load order groups are contained in the system registry, and determine the sequence that services are loaded into an operating system.</span></span> <span data-ttu-id="c97ff-177">Se o ponteiro for **nulo** ou apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="c97ff-177">If the pointer is **NULL**, or points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="c97ff-178">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="c97ff-178">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="c97ff-179">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="c97ff-179">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="c97ff-180">O registro do sistema tem uma lista de grupos de ordenação de carga localizados em **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="c97ff-180">The system registry has a list of load ordering groups located at **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-181">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-181">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-182">Lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-182">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="c97ff-183">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c97ff-183">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="c97ff-184">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="c97ff-184">If the pointer is **NULL**, or if it points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="c97ff-185">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="c97ff-185">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names, because services and service groups share the same namespace.</span></span> <span data-ttu-id="c97ff-186">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="c97ff-186">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-187">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c97ff-187">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-188">Lista que contém os nomes dos serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-188">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="c97ff-189">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c97ff-189">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="c97ff-190">Se o ponteiro for **nulo** ou apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="c97ff-190">If the pointer is **NULL**, or points to an empty string, the service does not have dependencies.</span></span> <span data-ttu-id="c97ff-191">A dependência de um serviço significa que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="c97ff-191">Dependency on a service means that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97ff-192">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c97ff-192">Return value</span></span>

<span data-ttu-id="c97ff-193">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c97ff-193">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c97ff-194">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="c97ff-194">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-195">0</span><span class="sxs-lookup"><span data-stu-id="c97ff-195">0</span></span>

<span data-ttu-id="c97ff-196">A solicitação é aceita.</span><span class="sxs-lookup"><span data-stu-id="c97ff-196">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-197">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="c97ff-197">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-198">1</span><span class="sxs-lookup"><span data-stu-id="c97ff-198">1</span></span>

<span data-ttu-id="c97ff-199">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="c97ff-199">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-200">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c97ff-200">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-201">2</span><span class="sxs-lookup"><span data-stu-id="c97ff-201">2</span></span>

<span data-ttu-id="c97ff-202">O usuário não tem os privilégios de acesso necessários.</span><span class="sxs-lookup"><span data-stu-id="c97ff-202">The user does not have the necessary access privileges.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-203">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="c97ff-203">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-204">3</span><span class="sxs-lookup"><span data-stu-id="c97ff-204">3</span></span>

<span data-ttu-id="c97ff-205">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="c97ff-205">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-206">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="c97ff-206">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-207">4</span><span class="sxs-lookup"><span data-stu-id="c97ff-207">4</span></span>

<span data-ttu-id="c97ff-208">O código de controle solicitado não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-208">The requested control code is not valid, or is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-209">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="c97ff-209">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-210">5</span><span class="sxs-lookup"><span data-stu-id="c97ff-210">5</span></span>

<span data-ttu-id="c97ff-211">O código de controle solicitado não pode ser enviado ao serviço porque a propriedade [**State**](win32-baseservice.md) no [**objeto \_ BaseService do Win32**](win32-baseservice.md) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="c97ff-211">The requested control code cannot be sent to the service because the [**State**](win32-baseservice.md) property in the [**Win32\_BaseService**](win32-baseservice.md) object is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-212">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="c97ff-212">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-213">6</span><span class="sxs-lookup"><span data-stu-id="c97ff-213">6</span></span>

<span data-ttu-id="c97ff-214">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-214">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-215">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="c97ff-215">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-216">7</span><span class="sxs-lookup"><span data-stu-id="c97ff-216">7</span></span>

<span data-ttu-id="c97ff-217">O serviço não responde à solicitação de início rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c97ff-217">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-218">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="c97ff-218">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-219">8</span><span class="sxs-lookup"><span data-stu-id="c97ff-219">8</span></span>

<span data-ttu-id="c97ff-220">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="c97ff-220">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-221">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="c97ff-221">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-222">9</span><span class="sxs-lookup"><span data-stu-id="c97ff-222">9</span></span>

<span data-ttu-id="c97ff-223">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-223">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-224">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="c97ff-224">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-225">10</span><span class="sxs-lookup"><span data-stu-id="c97ff-225">10</span></span>

<span data-ttu-id="c97ff-226">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="c97ff-226">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-227">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="c97ff-227">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-228">11</span><span class="sxs-lookup"><span data-stu-id="c97ff-228">11</span></span>

<span data-ttu-id="c97ff-229">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-229">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-230">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="c97ff-230">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-231">12</span><span class="sxs-lookup"><span data-stu-id="c97ff-231">12</span></span>

<span data-ttu-id="c97ff-232">Uma dependência para a qual esse serviço depende é removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-232">A dependency for which this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-233">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="c97ff-233">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-234">13</span><span class="sxs-lookup"><span data-stu-id="c97ff-234">13</span></span>

<span data-ttu-id="c97ff-235">O serviço não encontra o serviço necessário de um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="c97ff-235">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-236">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="c97ff-236">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-237">14</span><span class="sxs-lookup"><span data-stu-id="c97ff-237">14</span></span>

<span data-ttu-id="c97ff-238">O serviço está desabilitado no sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-238">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-239">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="c97ff-239">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-240">15</span><span class="sxs-lookup"><span data-stu-id="c97ff-240">15</span></span>

<span data-ttu-id="c97ff-241">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-241">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-242">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="c97ff-242">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-243">16</span><span class="sxs-lookup"><span data-stu-id="c97ff-243">16</span></span>

<span data-ttu-id="c97ff-244">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-244">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-245">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="c97ff-245">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-246">17</span><span class="sxs-lookup"><span data-stu-id="c97ff-246">17</span></span>

<span data-ttu-id="c97ff-247">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-247">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-248">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="c97ff-248">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-249">18</span><span class="sxs-lookup"><span data-stu-id="c97ff-249">18</span></span>

<span data-ttu-id="c97ff-250">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="c97ff-250">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-251">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="c97ff-251">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-252">19</span><span class="sxs-lookup"><span data-stu-id="c97ff-252">19</span></span>

<span data-ttu-id="c97ff-253">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="c97ff-253">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-254">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="c97ff-254">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-255">20</span><span class="sxs-lookup"><span data-stu-id="c97ff-255">20</span></span>

<span data-ttu-id="c97ff-256">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-256">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-257">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="c97ff-257">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-258">21</span><span class="sxs-lookup"><span data-stu-id="c97ff-258">21</span></span>

<span data-ttu-id="c97ff-259">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-259">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-260">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="c97ff-260">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-261">22</span><span class="sxs-lookup"><span data-stu-id="c97ff-261">22</span></span>

<span data-ttu-id="c97ff-262">A conta para a qual este serviço será executado não é válida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c97ff-262">The account for this service to run under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-263">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="c97ff-263">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-264">23</span><span class="sxs-lookup"><span data-stu-id="c97ff-264">23</span></span>

<span data-ttu-id="c97ff-265">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-265">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-266">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="c97ff-266">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-267">24</span><span class="sxs-lookup"><span data-stu-id="c97ff-267">24</span></span>

<span data-ttu-id="c97ff-268">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="c97ff-268">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c97ff-269">**Outras**</span><span class="sxs-lookup"><span data-stu-id="c97ff-269">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c97ff-270">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c97ff-270">25 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c97ff-271">Comentários</span><span class="sxs-lookup"><span data-stu-id="c97ff-271">Remarks</span></span>

<span data-ttu-id="c97ff-272">Para alterar um serviço de uma rede para um sistema local, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="c97ff-272">To change a service from a network to a local system, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="c97ff-273">Para alterar um serviço de um sistema local para uma rede, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :</span><span class="sxs-lookup"><span data-stu-id="c97ff-273">To change a service from a local system to a network, use the following values for the *StartName* and *StartPassword* parameters:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a><span data-ttu-id="c97ff-274">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c97ff-274">Requirements</span></span>



| <span data-ttu-id="c97ff-275">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97ff-275">Requirement</span></span> | <span data-ttu-id="c97ff-276">Valor</span><span class="sxs-lookup"><span data-stu-id="c97ff-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c97ff-277">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c97ff-277">Minimum supported client</span></span><br/> | <span data-ttu-id="c97ff-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c97ff-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c97ff-279">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c97ff-279">Minimum supported server</span></span><br/> | <span data-ttu-id="c97ff-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c97ff-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c97ff-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="c97ff-281">Namespace</span></span><br/>                | <span data-ttu-id="c97ff-282">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c97ff-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c97ff-283">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c97ff-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="c97ff-284"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c97ff-284"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="c97ff-285">MOF</span><span class="sxs-lookup"><span data-stu-id="c97ff-285">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c97ff-286"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c97ff-286"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c97ff-287">DLL</span><span class="sxs-lookup"><span data-stu-id="c97ff-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c97ff-288"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c97ff-288"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c97ff-289">Confira também</span><span class="sxs-lookup"><span data-stu-id="c97ff-289">See also</span></span>

<dl> <dt>

<span data-ttu-id="c97ff-290">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c97ff-290">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c97ff-291">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="c97ff-291">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

