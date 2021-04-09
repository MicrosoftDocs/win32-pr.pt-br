---
description: Cria um serviço novo.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Método Create da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c8115ed3d9795720796b5f944c11a519ff366983
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089155"
---
# <a name="create-method-of-the-win32_baseservice-class"></a><span data-ttu-id="c9a55-103">Método Create da classe Win32 \_ BaseService</span><span class="sxs-lookup"><span data-stu-id="c9a55-103">Create method of the Win32\_BaseService class</span></span>

<span data-ttu-id="c9a55-104">O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new service.</span></span> <span data-ttu-id="c9a55-105">O parâmetro *Loadordener* representa um agrupamento de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="c9a55-105">The *LoadOrderGroup* parameter represents a grouping of system services defining execution dependencies.</span></span> <span data-ttu-id="c9a55-106">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="c9a55-106">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="c9a55-107">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="c9a55-107">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="c9a55-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c9a55-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c9a55-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c9a55-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a55-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9a55-110">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c9a55-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9a55-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a55-112">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-113">Nome do serviço a ser instalado para o método **Create** .</span><span class="sxs-lookup"><span data-stu-id="c9a55-113">Name of the service to install to the **Create** method.</span></span> <span data-ttu-id="c9a55-114">O comprimento máximo da cadeia de caracteres é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c9a55-114">The maximum string length is 256 characters.</span></span> <span data-ttu-id="c9a55-115">O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres, mas comparações de nome de serviço sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c9a55-115">The service control manager database preserves the case of the characters, but service name comparisons are always case-insensitive.</span></span> <span data-ttu-id="c9a55-116">Barras invertidas (/) e barras invertidas duplas ( \\ ) são caracteres de nome de serviço inválidos.</span><span class="sxs-lookup"><span data-stu-id="c9a55-116">Forward-slashes (/) and double back-slashes (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-117">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-117">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-118">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-118">Display name of the service.</span></span> <span data-ttu-id="c9a55-119">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c9a55-119">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="c9a55-120">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-120">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="c9a55-121">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c9a55-121">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="c9a55-122">Restrições: aceita o mesmo valor que o parâmetro de *nome* .</span><span class="sxs-lookup"><span data-stu-id="c9a55-122">Constraints: Accepts the same value as the *Name* parameter.</span></span>

<span data-ttu-id="c9a55-123">Exemplo: "atdisk".</span><span class="sxs-lookup"><span data-stu-id="c9a55-123">Example: "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-124">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-124">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-125">Caminho totalmente qualificado para o arquivo executável que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-125">Fully qualified path to the executable file that implements the service.</span></span>

<span data-ttu-id="c9a55-126">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="c9a55-126">Example: "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-127">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-127">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-128">Tipo de serviços fornecidos para processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="c9a55-128">Type of services provided to processes that call them.</span></span> <span data-ttu-id="c9a55-129">O valor é um bitmap.</span><span class="sxs-lookup"><span data-stu-id="c9a55-129">The value is a bitmap.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="c9a55-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver de kernel** (1)</span><span class="sxs-lookup"><span data-stu-id="c9a55-130"><span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="c9a55-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver do sistema de arquivos** (2)</span><span class="sxs-lookup"><span data-stu-id="c9a55-131"><span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**File System Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="c9a55-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)</span><span class="sxs-lookup"><span data-stu-id="c9a55-132"><span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="c9a55-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver do reconhecedor** (8)</span><span class="sxs-lookup"><span data-stu-id="c9a55-133"><span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="c9a55-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Próprio processo** (16)</span><span class="sxs-lookup"><span data-stu-id="c9a55-134"><span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Own Process** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="c9a55-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo de compartilhamento** (32)</span><span class="sxs-lookup"><span data-stu-id="c9a55-135"><span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Share Process** (32)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="c9a55-136">256</span><span class="sxs-lookup"><span data-stu-id="c9a55-136">256</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-137">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="c9a55-137">Interactive Process</span></span>

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c9a55-138">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-138">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-139">Severidade do erro se o método **Create** falhar ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="c9a55-139">Severity of the error if the **Create** method fails to start.</span></span> <span data-ttu-id="c9a55-140">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="c9a55-140">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="c9a55-141">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-141">All errors are logged by the system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="c9a55-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** (0)</span><span class="sxs-lookup"><span data-stu-id="c9a55-142"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-143">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-143">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="c9a55-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="c9a55-144"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-145">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-145">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="c9a55-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severo** (2)</span><span class="sxs-lookup"><span data-stu-id="c9a55-146"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-147">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="c9a55-147">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="c9a55-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="c9a55-148"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-149">O sistema tenta iniciar com uma configuração válida.</span><span class="sxs-lookup"><span data-stu-id="c9a55-149">System attempts to start with a good configuration.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c9a55-150">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-150">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-151">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="c9a55-151">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="c9a55-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="c9a55-152"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-153">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c9a55-153">Device driver started by the operating system loader.</span></span> <span data-ttu-id="c9a55-154">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="c9a55-154">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="c9a55-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="c9a55-155"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-156">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c9a55-156">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c9a55-157">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="c9a55-157">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="c9a55-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="c9a55-158"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-159">Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-159">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="c9a55-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")</span><span class="sxs-lookup"><span data-stu-id="c9a55-160"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-161">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a55-161">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c9a55-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="c9a55-162"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="c9a55-163">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-163">Service that can no longer be started.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c9a55-164">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-164">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-165">Se **for true**, o serviço poderá criar ou se comunicar com o Windows na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c9a55-165">If **true**, the service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-166">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-166">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-167">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-167">Account name under which the service runs.</span></span> <span data-ttu-id="c9a55-168">Dependendo do tipo de serviço, o nome da conta pode estar na forma de "DomainName \\ username".</span><span class="sxs-lookup"><span data-stu-id="c9a55-168">Depending on the service type, the account name may be in the form of "DomainName\\Username".</span></span> <span data-ttu-id="c9a55-169">O processo de serviço é registrado usando uma dessas duas formas quando é executado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-169">The service process is logged using one of these two forms when it runs.</span></span> <span data-ttu-id="c9a55-170">Se a conta pertencer ao domínio interno, ". \\ Username "pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-170">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="c9a55-171">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="c9a55-171">If **NULL** is specified, the service is logged on as the LocalSystem account.</span></span> <span data-ttu-id="c9a55-172">Para um kernel ou drivers de nível de sistema, o *StartName* contém o nome do objeto de driver (ou seja, o sistema de \\ arquivos \\ rdr ou \\ \\ o driver XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c9a55-172">For a kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="c9a55-173">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-173">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="c9a55-174">Exemplo: DWDOM \\ admin.</span><span class="sxs-lookup"><span data-stu-id="c9a55-174">Example: DWDOM\\Admin.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-175">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-175">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-176">Senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="c9a55-176">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="c9a55-177">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="c9a55-177">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="c9a55-178">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="c9a55-178">Specify an empty string if the service has no password.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-179">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-179">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-180">Nome do grupo associado ao novo serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-180">Group name associated with the new service.</span></span> <span data-ttu-id="c9a55-181">Os grupos de ordem de carregamento estão contidos no registro e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c9a55-181">Load order groups are contained in the registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="c9a55-182">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="c9a55-182">If the pointer is **NULL** or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="c9a55-183">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="c9a55-183">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="c9a55-184">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="c9a55-184">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="c9a55-185">O registro tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="c9a55-185">The registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="c9a55-186">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="c9a55-186">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-187">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-187">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-188">Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-188">Array of load-ordering groups that must start before this service.</span></span> <span data-ttu-id="c9a55-189">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="c9a55-189">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="c9a55-190">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="c9a55-190">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="c9a55-191">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="c9a55-191">If the pointer is **NULL** or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="c9a55-192">Os nomes de grupo devem ser prefixados pelo \_ identificador do grupo SC \_ (definido no arquivo Winsvc. h) para diferenciá-lo de um nome de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="c9a55-192">Group names must be prefixed by the SC\_GROUP\_IDENTIFIER (defined in the Winsvc.h file) character to differentiate it from a service name, because services and service groups share the same namespace.</span></span> <span data-ttu-id="c9a55-193">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="c9a55-193">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-194">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9a55-194">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-195">Matriz que contém nomes de serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-195">Array that contains names of services that must start before this service starts.</span></span> <span data-ttu-id="c9a55-196">Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** .</span><span class="sxs-lookup"><span data-stu-id="c9a55-196">Each item in the array is delimited by **NULL** and the list is terminated by two **NULL** values.</span></span> <span data-ttu-id="c9a55-197">Em Visual Basic ou script, você pode passar um vbArray.</span><span class="sxs-lookup"><span data-stu-id="c9a55-197">In Visual Basic or script you can pass a vbArray.</span></span> <span data-ttu-id="c9a55-198">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="c9a55-198">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="c9a55-199">A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="c9a55-199">Dependency on a service means that this service can only run if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a55-200">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9a55-200">Return value</span></span>

<span data-ttu-id="c9a55-201">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c9a55-201">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c9a55-202">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="c9a55-202">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-203">0</span><span class="sxs-lookup"><span data-stu-id="c9a55-203">0</span></span>

<span data-ttu-id="c9a55-204">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="c9a55-204">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-205">**Sem suporte**</span><span class="sxs-lookup"><span data-stu-id="c9a55-205">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-206">1</span><span class="sxs-lookup"><span data-stu-id="c9a55-206">1</span></span>

<span data-ttu-id="c9a55-207">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="c9a55-207">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-208">**Acesso negado**</span><span class="sxs-lookup"><span data-stu-id="c9a55-208">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-209">2</span><span class="sxs-lookup"><span data-stu-id="c9a55-209">2</span></span>

<span data-ttu-id="c9a55-210">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="c9a55-210">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-211">**Serviços dependentes em execução**</span><span class="sxs-lookup"><span data-stu-id="c9a55-211">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-212">3</span><span class="sxs-lookup"><span data-stu-id="c9a55-212">3</span></span>

<span data-ttu-id="c9a55-213">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="c9a55-213">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-214">**Controle de serviço inválido**</span><span class="sxs-lookup"><span data-stu-id="c9a55-214">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-215">4</span><span class="sxs-lookup"><span data-stu-id="c9a55-215">4</span></span>

<span data-ttu-id="c9a55-216">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-216">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-217">**O serviço não pode aceitar o controle**</span><span class="sxs-lookup"><span data-stu-id="c9a55-217">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-218">5</span><span class="sxs-lookup"><span data-stu-id="c9a55-218">5</span></span>

<span data-ttu-id="c9a55-219">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="c9a55-219">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-220">**Serviço não ativo**</span><span class="sxs-lookup"><span data-stu-id="c9a55-220">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-221">6</span><span class="sxs-lookup"><span data-stu-id="c9a55-221">6</span></span>

<span data-ttu-id="c9a55-222">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-222">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-223">**Tempo limite da solicitação de serviço**</span><span class="sxs-lookup"><span data-stu-id="c9a55-223">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-224">7</span><span class="sxs-lookup"><span data-stu-id="c9a55-224">7</span></span>

<span data-ttu-id="c9a55-225">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="c9a55-225">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-226">**Falha desconhecida**</span><span class="sxs-lookup"><span data-stu-id="c9a55-226">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-227">8</span><span class="sxs-lookup"><span data-stu-id="c9a55-227">8</span></span>

<span data-ttu-id="c9a55-228">Processo interativo.</span><span class="sxs-lookup"><span data-stu-id="c9a55-228">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-229">**Caminho não encontrado**</span><span class="sxs-lookup"><span data-stu-id="c9a55-229">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-230">9</span><span class="sxs-lookup"><span data-stu-id="c9a55-230">9</span></span>

<span data-ttu-id="c9a55-231">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-231">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-232">**Serviço já em execução**</span><span class="sxs-lookup"><span data-stu-id="c9a55-232">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-233">10</span><span class="sxs-lookup"><span data-stu-id="c9a55-233">10</span></span>

<span data-ttu-id="c9a55-234">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="c9a55-234">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-235">**Banco de dados de serviço bloqueado**</span><span class="sxs-lookup"><span data-stu-id="c9a55-235">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-236">11</span><span class="sxs-lookup"><span data-stu-id="c9a55-236">11</span></span>

<span data-ttu-id="c9a55-237">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-237">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-238">**Dependência de serviço excluída**</span><span class="sxs-lookup"><span data-stu-id="c9a55-238">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-239">12</span><span class="sxs-lookup"><span data-stu-id="c9a55-239">12</span></span>

<span data-ttu-id="c9a55-240">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-240">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-241">**Falha na dependência de serviço**</span><span class="sxs-lookup"><span data-stu-id="c9a55-241">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-242">13</span><span class="sxs-lookup"><span data-stu-id="c9a55-242">13</span></span>

<span data-ttu-id="c9a55-243">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="c9a55-243">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-244">**Serviço desabilitado**</span><span class="sxs-lookup"><span data-stu-id="c9a55-244">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-245">14</span><span class="sxs-lookup"><span data-stu-id="c9a55-245">14</span></span>

<span data-ttu-id="c9a55-246">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-246">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-247">**Falha no logon do serviço**</span><span class="sxs-lookup"><span data-stu-id="c9a55-247">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-248">15</span><span class="sxs-lookup"><span data-stu-id="c9a55-248">15</span></span>

<span data-ttu-id="c9a55-249">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-249">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-250">**Serviço marcado para exclusão**</span><span class="sxs-lookup"><span data-stu-id="c9a55-250">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-251">16</span><span class="sxs-lookup"><span data-stu-id="c9a55-251">16</span></span>

<span data-ttu-id="c9a55-252">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-252">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-253">**Serviço sem thread**</span><span class="sxs-lookup"><span data-stu-id="c9a55-253">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-254">17</span><span class="sxs-lookup"><span data-stu-id="c9a55-254">17</span></span>

<span data-ttu-id="c9a55-255">Não há nenhum thread de execução para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-255">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-256">**Dependência circular de status**</span><span class="sxs-lookup"><span data-stu-id="c9a55-256">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-257">18</span><span class="sxs-lookup"><span data-stu-id="c9a55-257">18</span></span>

<span data-ttu-id="c9a55-258">Há dependências circulares quando o serviço é iniciado.</span><span class="sxs-lookup"><span data-stu-id="c9a55-258">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-259">**Nome duplicado de status**</span><span class="sxs-lookup"><span data-stu-id="c9a55-259">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-260">19</span><span class="sxs-lookup"><span data-stu-id="c9a55-260">19</span></span>

<span data-ttu-id="c9a55-261">Há um serviço em execução com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="c9a55-261">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-262">**Nome inválido do status**</span><span class="sxs-lookup"><span data-stu-id="c9a55-262">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-263">20</span><span class="sxs-lookup"><span data-stu-id="c9a55-263">20</span></span>

<span data-ttu-id="c9a55-264">Há caracteres inválidos no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-264">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-265">**Parâmetro de status inválido**</span><span class="sxs-lookup"><span data-stu-id="c9a55-265">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-266">21</span><span class="sxs-lookup"><span data-stu-id="c9a55-266">21</span></span>

<span data-ttu-id="c9a55-267">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-267">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-268">**Conta de serviço inválida de status**</span><span class="sxs-lookup"><span data-stu-id="c9a55-268">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-269">22</span><span class="sxs-lookup"><span data-stu-id="c9a55-269">22</span></span>

<span data-ttu-id="c9a55-270">A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="c9a55-270">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-271">**O serviço de status existe**</span><span class="sxs-lookup"><span data-stu-id="c9a55-271">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-272">23</span><span class="sxs-lookup"><span data-stu-id="c9a55-272">23</span></span>

<span data-ttu-id="c9a55-273">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-273">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-274">**O serviço já está em pausa**</span><span class="sxs-lookup"><span data-stu-id="c9a55-274">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-275">24</span><span class="sxs-lookup"><span data-stu-id="c9a55-275">24</span></span>

<span data-ttu-id="c9a55-276">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="c9a55-276">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c9a55-277">**Outras**</span><span class="sxs-lookup"><span data-stu-id="c9a55-277">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c9a55-278">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="c9a55-278">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9a55-279">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a55-279">Requirements</span></span>



| <span data-ttu-id="c9a55-280">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a55-280">Requirement</span></span> | <span data-ttu-id="c9a55-281">Valor</span><span class="sxs-lookup"><span data-stu-id="c9a55-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a55-282">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9a55-282">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a55-283">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9a55-283">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9a55-284">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9a55-284">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a55-285">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9a55-285">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9a55-286">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9a55-286">Namespace</span></span><br/>                | <span data-ttu-id="c9a55-287">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c9a55-287">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9a55-288">MOF</span><span class="sxs-lookup"><span data-stu-id="c9a55-288">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9a55-289"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9a55-289"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9a55-290">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a55-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a55-291"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a55-291"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a55-292">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9a55-292">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9a55-293">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9a55-293">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c9a55-294">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="c9a55-294">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

