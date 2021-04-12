---
title: Classe Win32_TerminalService
description: Uma subclasse da classe de serviço do Win32 \_ . O Win32 \_ TerminalService representa a propriedade Element da \_ Associação Win32 TerminalServiceToSetting.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TerminalService Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TerminalService classe, descrita
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455855"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="c11af-106">\_Classe Win32 TerminalService</span><span class="sxs-lookup"><span data-stu-id="c11af-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="c11af-107">A classe WMI **\_ TerminalService do Win32** é uma subclasse da classe [**de \_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="c11af-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="c11af-108">**Win32 \_ TerminalService** representa a propriedade **Element** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="c11af-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="c11af-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="c11af-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c11af-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c11af-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="c11af-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c11af-111">Members</span></span>

<span data-ttu-id="c11af-112">A classe **Win32 \_ TerminalService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c11af-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="c11af-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c11af-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c11af-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c11af-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c11af-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c11af-115">Methods</span></span>

<span data-ttu-id="c11af-116">A classe **Win32 \_ TerminalService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c11af-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="c11af-117">Método</span><span class="sxs-lookup"><span data-stu-id="c11af-117">Method</span></span>                                                                       | <span data-ttu-id="c11af-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c11af-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c11af-119">**Alteração**</span><span class="sxs-lookup"><span data-stu-id="c11af-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="c11af-120">Modifica um serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="c11af-121">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="c11af-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="c11af-122">Modifica o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="c11af-123">**Criar**</span><span class="sxs-lookup"><span data-stu-id="c11af-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="c11af-124">Cria um serviço novo.</span><span class="sxs-lookup"><span data-stu-id="c11af-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="c11af-125">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="c11af-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="c11af-126">Exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="c11af-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="c11af-127">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c11af-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="c11af-128">Retorna o descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="c11af-129">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="c11af-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="c11af-130">Solicita que um serviço atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="c11af-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="c11af-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="c11af-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="c11af-132">Tenta colocar um serviço no estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="c11af-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="c11af-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="c11af-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="c11af-134">Tenta posicionar um serviço no estado retomado.</span><span class="sxs-lookup"><span data-stu-id="c11af-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="c11af-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c11af-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="c11af-136">Grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="c11af-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c11af-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="c11af-138">Tenta posicionar um serviço no estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="c11af-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="c11af-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c11af-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="c11af-140">Coloca um serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="c11af-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="c11af-141">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="c11af-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="c11af-142">Tenta enviar um código de controle definido pelo usuário para um serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="c11af-143">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c11af-143">Properties</span></span>

<span data-ttu-id="c11af-144">A classe **Win32 \_ TerminalService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c11af-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c11af-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="c11af-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c11af-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ Pause \_ Continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("o serviço aceita Pause")</span><span class="sxs-lookup"><span data-stu-id="c11af-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-149">Indica se o serviço pode ser pausado.</span><span class="sxs-lookup"><span data-stu-id="c11af-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="c11af-150">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="c11af-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-152">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c11af-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-154">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| Service \_ Accept \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("o serviço aceita Stop")</span><span class="sxs-lookup"><span data-stu-id="c11af-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-155">Indica se o serviço pode ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="c11af-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="c11af-156">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-157">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c11af-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-160">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c11af-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-161">Breve descrição do serviço de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="c11af-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="c11af-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c11af-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-163">**Verifica**</span><span class="sxs-lookup"><span data-stu-id="c11af-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-164">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-166">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("contagem de pontos de verificação")</span><span class="sxs-lookup"><span data-stu-id="c11af-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-167">Valor que o serviço incrementa periodicamente para relatar seu progresso durante uma longa operação de início, parada, pausa ou continuação.</span><span class="sxs-lookup"><span data-stu-id="c11af-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="c11af-168">Por exemplo, o serviço incrementa esse valor à medida que ele conclui cada etapa de sua inicialização quando ele está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="c11af-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="c11af-169">O programa de interface do usuário que invoca a operação no serviço usa esse valor para acompanhar o progresso do serviço durante uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="c11af-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="c11af-170">Esse valor não é válido e deve ser zero quando o serviço não tem uma operação de início, parada, pausa ou continuação pendente.</span><span class="sxs-lookup"><span data-stu-id="c11af-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="c11af-171">Essa propriedade é herdada [**do \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c11af-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-175">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="c11af-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-176">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c11af-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c11af-177">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c11af-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c11af-178">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="c11af-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-180">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c11af-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-182">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("as \| estruturas de serviço win32api \| [**serviço de \_ \_ início automático atrasado de \_ \_ informações**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("início automático atrasado")</span><span class="sxs-lookup"><span data-stu-id="c11af-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-183">Se **for true**, o serviço será iniciado depois que outros serviços de início automático forem iniciados além de um pequeno atraso.</span><span class="sxs-lookup"><span data-stu-id="c11af-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="c11af-184">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c11af-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="c11af-185">Essa propriedade é herdada [**do \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-186">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c11af-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-189">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c11af-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-190">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="c11af-190">Description of the object.</span></span>

<span data-ttu-id="c11af-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c11af-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="c11af-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-193">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c11af-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-195">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| processo interativo do serviço \_ \_ "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interage com a área de trabalho")</span><span class="sxs-lookup"><span data-stu-id="c11af-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-196">Indica se o serviço pode criar ou se comunicar com o Windows na área de trabalho e, portanto, interagir de alguma maneira com um usuário.</span><span class="sxs-lookup"><span data-stu-id="c11af-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="c11af-197">Os serviços interativos devem ser executados na conta sistema local.</span><span class="sxs-lookup"><span data-stu-id="c11af-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="c11af-198">A maioria dos serviços não são interativos; ou seja, eles não se comunicam com o usuário de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="c11af-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="c11af-199">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-200">**DisconnectedSessions**</span><span class="sxs-lookup"><span data-stu-id="c11af-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c11af-203">O número de sessões desconectadas no servidor atual.</span><span class="sxs-lookup"><span data-stu-id="c11af-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="c11af-204">Essas sessões ainda podem estar ativamente consumindo recursos do servidor, no entanto, atualmente, não têm nenhuma conexão de rede com um cliente.</span><span class="sxs-lookup"><span data-stu-id="c11af-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="c11af-205">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c11af-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-208">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta da \| [**\_ \_ configuração do serviço**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome de exibição")</span><span class="sxs-lookup"><span data-stu-id="c11af-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-209">Nome do serviço como exibido no snap-in serviços.</span><span class="sxs-lookup"><span data-stu-id="c11af-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="c11af-210">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="c11af-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="c11af-211">Observe que o nome de exibição e o nome do serviço (que é armazenado no registro) nem sempre são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="c11af-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="c11af-212">Por exemplo, o serviço de cliente DHCP tem o nome de serviço DHCP, mas o nome de exibição cliente DHCP.</span><span class="sxs-lookup"><span data-stu-id="c11af-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="c11af-213">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="c11af-214">No entanto, as comparações [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c11af-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="c11af-215">Restrição: aceita o mesmo valor que a propriedade [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="c11af-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="c11af-216">Exemplo: "atdisk"</span><span class="sxs-lookup"><span data-stu-id="c11af-216">Example: "Atdisk"</span></span>

<span data-ttu-id="c11af-217">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="c11af-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-221">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| do serviço de \| [**consulta da \_ \_ configuração do serviço**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("severidade de falha na inicialização")</span><span class="sxs-lookup"><span data-stu-id="c11af-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-222">Severidade do erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="c11af-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="c11af-223">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="c11af-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="c11af-224">Todos os erros são anotados pelo sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="c11af-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="c11af-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("ignorar")</span><span class="sxs-lookup"><span data-stu-id="c11af-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-226">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="c11af-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="c11af-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="c11af-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-228">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="c11af-228">User is notified.</span></span> <span data-ttu-id="c11af-229">Normalmente, essa será uma caixa de mensagem exibida notificando o usuário do problema.</span><span class="sxs-lookup"><span data-stu-id="c11af-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="c11af-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("severo")</span><span class="sxs-lookup"><span data-stu-id="c11af-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-231">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="c11af-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="c11af-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="c11af-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-233">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="c11af-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="c11af-234">Se o serviço não for iniciado pela segunda vez, a inicialização falhará.</span><span class="sxs-lookup"><span data-stu-id="c11af-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c11af-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c11af-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-236">A severidade do erro é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="c11af-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="c11af-237">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-238">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="c11af-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-239">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-241">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de saída")</span><span class="sxs-lookup"><span data-stu-id="c11af-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-242">Código de erro do Windows que define os erros encontrados ao iniciar ou interromper o serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="c11af-243">Essa propriedade é definida como **\_ \_ \_ erro específico do serviço de erro** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="c11af-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="c11af-244">O serviço define esse valor como **sem \_ erros** durante a execução e novamente após o término normal.</span><span class="sxs-lookup"><span data-stu-id="c11af-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="c11af-245">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c11af-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-247">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c11af-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-249">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c11af-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-250">O objeto de data está instalado.</span><span class="sxs-lookup"><span data-stu-id="c11af-250">Date object is installed.</span></span> <span data-ttu-id="c11af-251">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c11af-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c11af-252">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c11af-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-253">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c11af-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-256">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c11af-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c11af-257">Identificador exclusivo do serviço que fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="c11af-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="c11af-258">Essa funcionalidade é descrita na propriedade [**Descrição**](/windows/desktop/CIMWin32Prov/win32-service) do objeto.</span><span class="sxs-lookup"><span data-stu-id="c11af-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="c11af-259">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c11af-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="c11af-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-263">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do caminho do arquivo")</span><span class="sxs-lookup"><span data-stu-id="c11af-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-264">Caminho totalmente qualificado para o arquivo binário de serviço que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="c11af-265">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="c11af-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="c11af-266">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-267">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="c11af-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-268">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-270">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| código de status do serviço de estruturas de serviço win32api \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| DwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID do processo")</span><span class="sxs-lookup"><span data-stu-id="c11af-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-271">Identificador do processo do serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-271">Process identifier of the service.</span></span>

<span data-ttu-id="c11af-272">Exemplo: 324</span><span class="sxs-lookup"><span data-stu-id="c11af-272">Example: 324</span></span>

<span data-ttu-id="c11af-273">Essa propriedade é herdada [**do \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-274">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="c11af-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-275">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-277">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de saída específico do servidor")</span><span class="sxs-lookup"><span data-stu-id="c11af-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-278">Código de erro específico do serviço para erros que ocorrem enquanto o serviço está sendo iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="c11af-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="c11af-279">Os códigos de saída são definidos pelo serviço representado por essa classe.</span><span class="sxs-lookup"><span data-stu-id="c11af-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="c11af-280">Esse valor só é definido quando o valor da propriedade [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) é um **\_ \_ \_ erro específico do serviço de erro** (1066).</span><span class="sxs-lookup"><span data-stu-id="c11af-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="c11af-281">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="c11af-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-283">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-284">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-285">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de serviço")</span><span class="sxs-lookup"><span data-stu-id="c11af-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-286">Tipo de serviço fornecido a processos de chamada.</span><span class="sxs-lookup"><span data-stu-id="c11af-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="c11af-287">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="c11af-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="c11af-288">**Driver de kernel** ("driver de kernel")</span><span class="sxs-lookup"><span data-stu-id="c11af-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="c11af-289">**Driver do sistema de arquivos** ("driver do sistema de arquivos")</span><span class="sxs-lookup"><span data-stu-id="c11af-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="c11af-290">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="c11af-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="c11af-291">**Driver do reconhecedor** ("driver do reconhecedor")</span><span class="sxs-lookup"><span data-stu-id="c11af-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="c11af-292">**Próprio processo** ("processo próprio")</span><span class="sxs-lookup"><span data-stu-id="c11af-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="c11af-293">**Processo de compartilhamento** ("processo de compartilhamento")</span><span class="sxs-lookup"><span data-stu-id="c11af-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="c11af-294">**Processo interativo** ("processo interativo")</span><span class="sxs-lookup"><span data-stu-id="c11af-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="c11af-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c11af-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="c11af-296">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-297">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="c11af-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-298">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c11af-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-300">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="c11af-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-301">Indica se o serviço é iniciado ou não.</span><span class="sxs-lookup"><span data-stu-id="c11af-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="c11af-302">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-303">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c11af-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-306">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="c11af-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-307">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="c11af-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="c11af-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="c11af-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-309">Driver de dispositivo iniciado pelo carregador do sistema operacional (válido somente para serviços de driver).</span><span class="sxs-lookup"><span data-stu-id="c11af-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="c11af-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="c11af-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-311">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c11af-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="c11af-312">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="c11af-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="c11af-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automático** ("auto")</span><span class="sxs-lookup"><span data-stu-id="c11af-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-314">Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="c11af-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="c11af-315">Os serviços automáticos são iniciados mesmo se um usuário não fizer logon.</span><span class="sxs-lookup"><span data-stu-id="c11af-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="c11af-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="c11af-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-317">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="c11af-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="c11af-318">Esses serviços não são iniciados, a menos que um usuário faça logon e os inicie.</span><span class="sxs-lookup"><span data-stu-id="c11af-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c11af-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="c11af-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="c11af-320">Serviço que não pode ser iniciado até que seu StartMode seja alterado para automático ou manual.</span><span class="sxs-lookup"><span data-stu-id="c11af-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="c11af-321">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="c11af-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-325">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da conta inicial")</span><span class="sxs-lookup"><span data-stu-id="c11af-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-326">Nome da conta sob a qual um serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="c11af-326">Account name under which a service runs.</span></span> <span data-ttu-id="c11af-327">Dependendo do tipo de serviço, o nome da conta pode estar na forma de "DomainName \\ username" ou do formato UPN (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="c11af-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="c11af-328">O processo de serviço é registrado usando uma dessas duas formas quando é executado.</span><span class="sxs-lookup"><span data-stu-id="c11af-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="c11af-329">Se a conta pertencer ao domínio interno, então ". \\ Username "pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c11af-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="c11af-330">Para drivers de nível de kernel ou de sistema, o [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contém o nome do objeto de driver (ou seja, " \\ FileSystem \\ rdr" ou " \\ Driver \\ XNS") que o sistema de e/s usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c11af-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="c11af-331">Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="c11af-332">Exemplo: "administrador do DWDOM \\ "</span><span class="sxs-lookup"><span data-stu-id="c11af-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="c11af-333">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-334">**State**</span><span class="sxs-lookup"><span data-stu-id="c11af-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-336">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="c11af-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c11af-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="c11af-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-338">Estado atual do serviço base.</span><span class="sxs-lookup"><span data-stu-id="c11af-338">Current state of the base service.</span></span>

<span data-ttu-id="c11af-339">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="c11af-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="c11af-340">**Parado** ("parado")</span><span class="sxs-lookup"><span data-stu-id="c11af-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="c11af-341">**Início pendente** ("início pendente")</span><span class="sxs-lookup"><span data-stu-id="c11af-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="c11af-342">**Parada pendente** ("parar pendente")</span><span class="sxs-lookup"><span data-stu-id="c11af-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c11af-343">**Em execução** ("em execução")</span><span class="sxs-lookup"><span data-stu-id="c11af-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="c11af-344">**Continuação pendente** ("continuar pendente")</span><span class="sxs-lookup"><span data-stu-id="c11af-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="c11af-345">**Pausa pendente** ("pausa pendente")</span><span class="sxs-lookup"><span data-stu-id="c11af-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c11af-346">Em **pausa** ("pausado")</span><span class="sxs-lookup"><span data-stu-id="c11af-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c11af-347">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c11af-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="c11af-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c11af-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="c11af-349">**Windows Server 2008 e Windows Vista:** Essa propriedade é somente leitura antes do Windows 7 e do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c11af-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="c11af-350">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-351">**Status**</span><span class="sxs-lookup"><span data-stu-id="c11af-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-354">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c11af-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-355">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c11af-355">Current status of the object.</span></span> <span data-ttu-id="c11af-356">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c11af-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c11af-357">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c11af-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c11af-358">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c11af-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c11af-359">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c11af-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c11af-360">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c11af-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c11af-361">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="c11af-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c11af-362">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c11af-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c11af-363">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c11af-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c11af-364">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c11af-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c11af-365">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c11af-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c11af-366">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c11af-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c11af-367">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c11af-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c11af-368">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c11af-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c11af-369">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c11af-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c11af-370">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c11af-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c11af-371">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c11af-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c11af-372">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c11af-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c11af-373">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c11af-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c11af-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c11af-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="c11af-375">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c11af-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-376">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c11af-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-377">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-379">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="c11af-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-380">Digite o nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="c11af-381">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-382">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c11af-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-383">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c11af-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-385">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="c11af-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-386">Nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="c11af-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="c11af-387">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-388">**TagId**</span><span class="sxs-lookup"><span data-stu-id="c11af-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-389">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-391">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID da marca")</span><span class="sxs-lookup"><span data-stu-id="c11af-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-392">Valor de marca exclusivo para este serviço no grupo.</span><span class="sxs-lookup"><span data-stu-id="c11af-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="c11af-393">Um valor de 0 (zero) indica que o serviço não tem uma marca.</span><span class="sxs-lookup"><span data-stu-id="c11af-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="c11af-394">Uma marca pode ser usada para ordenar a inicialização do serviço dentro de um grupo de ordem de carregamento, especificando um vetor de ordem de marca no Registro localizado em:</span><span class="sxs-lookup"><span data-stu-id="c11af-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="c11af-395">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **GroupOrderList**    </span><span class="sxs-lookup"><span data-stu-id="c11af-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="c11af-396">As marcas são avaliadas somente para os serviços de tipo de inicialização driver de kernel e driver de sistema de arquivos que têm os modos de inicialização do sistema ou inicializados.</span><span class="sxs-lookup"><span data-stu-id="c11af-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="c11af-397">Esta propriedade é herdada do [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="c11af-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="c11af-398">**TotalSessions**</span><span class="sxs-lookup"><span data-stu-id="c11af-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-399">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c11af-401">O número total de sessões no servidor atual.</span><span class="sxs-lookup"><span data-stu-id="c11af-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="c11af-402">Isso inclui sessões conectadas e desconectadas.</span><span class="sxs-lookup"><span data-stu-id="c11af-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="c11af-403">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="c11af-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c11af-404">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c11af-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c11af-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c11af-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c11af-406">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo de espera estimado")</span><span class="sxs-lookup"><span data-stu-id="c11af-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="c11af-407">Tempo estimado necessário, em milissegundos, para uma operação de início, parada, pausa ou continuação pendente.</span><span class="sxs-lookup"><span data-stu-id="c11af-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="c11af-408">Depois que o tempo especificado tiver decorrido, o serviço fará sua próxima chamada para o método **falha em SetServiceStatus** com um valor de [**ponto de verificação**](/windows/desktop/CIMWin32Prov/win32-service) incrementado ou uma alteração no **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="c11af-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="c11af-409">Se o tempo especificado por **WaitHint** passa e o ponto de **verificação** não tiver sido incrementado ou **CurrentState** não tiver sido alterado, o Gerenciador de controle de serviço ou o programa de controle de serviço assumirá que ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="c11af-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="c11af-410">Essa propriedade é herdada [**do \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="c11af-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c11af-411">Comentários</span><span class="sxs-lookup"><span data-stu-id="c11af-411">Remarks</span></span>

<span data-ttu-id="c11af-412">Como a classe **Win32 \_ TerminalService** é uma subclasse da classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) , a classe herda todas as propriedades e métodos do **\_ serviço Win32**.</span><span class="sxs-lookup"><span data-stu-id="c11af-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="c11af-413">[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) está associado ao **Win32 \_ TerminalService** como a propriedade **Setting** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="c11af-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="c11af-414">[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) está associado ao **Win32 \_ TerminalService** como a propriedade **Setting** da Associação [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="c11af-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="c11af-415">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c11af-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c11af-416">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c11af-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c11af-417">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c11af-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c11af-418">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c11af-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c11af-419">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c11af-419">Requirements</span></span>



| <span data-ttu-id="c11af-420">Requisito</span><span class="sxs-lookup"><span data-stu-id="c11af-420">Requirement</span></span> | <span data-ttu-id="c11af-421">Valor</span><span class="sxs-lookup"><span data-stu-id="c11af-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c11af-422">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c11af-422">Minimum supported client</span></span><br/> | <span data-ttu-id="c11af-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c11af-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c11af-424">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c11af-424">Minimum supported server</span></span><br/> | <span data-ttu-id="c11af-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c11af-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c11af-426">Namespace</span><span class="sxs-lookup"><span data-stu-id="c11af-426">Namespace</span></span><br/>                | <span data-ttu-id="c11af-427">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c11af-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="c11af-428">MOF</span><span class="sxs-lookup"><span data-stu-id="c11af-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c11af-429"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c11af-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c11af-430">DLL</span><span class="sxs-lookup"><span data-stu-id="c11af-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c11af-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c11af-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c11af-432">Confira também</span><span class="sxs-lookup"><span data-stu-id="c11af-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c11af-433">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="c11af-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="c11af-434">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c11af-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="c11af-435">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="c11af-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="c11af-436">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="c11af-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="c11af-437">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="c11af-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

