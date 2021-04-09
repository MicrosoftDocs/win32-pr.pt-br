---
description: A \_ classe WMI abstrata do Win32 BaseService representa objetos executáveis que são instalados em um banco de dados do Registro mantido pelo Gerenciador de controle de serviço.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089540"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="a57b6-103">\_Classe Win32 BaseService</span><span class="sxs-lookup"><span data-stu-id="a57b6-103">Win32\_BaseService class</span></span>

<span data-ttu-id="a57b6-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstrata do **Win32 \_ BaseService** representa objetos executáveis que são instalados em um banco de dados do Registro mantido pelo Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="a57b6-105">O arquivo executável associado a um serviço pode ser iniciado no momento da inicialização por um programa de inicialização ou pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a57b6-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="a57b6-106">Ele também pode ser iniciado sob demanda pelo Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="a57b6-107">Qualquer serviço ou processo que não seja de propriedade de um usuário específico, e que forneça uma interface para algumas funcionalidades com suporte no sistema de computador, é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a57b6-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="a57b6-108">Exemplo: o serviço de cliente do protocolo DHCP em um sistema de computador que executa o Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a57b6-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="a57b6-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a57b6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a57b6-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a57b6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57b6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a57b6-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="a57b6-112">Membros</span><span class="sxs-lookup"><span data-stu-id="a57b6-112">Members</span></span>

<span data-ttu-id="a57b6-113">A classe **Win32 \_ BaseService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a57b6-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="a57b6-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a57b6-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="a57b6-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a57b6-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a57b6-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="a57b6-116">Methods</span></span>

<span data-ttu-id="a57b6-117">A classe **Win32 \_ BaseService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a57b6-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="a57b6-118">Método</span><span class="sxs-lookup"><span data-stu-id="a57b6-118">Method</span></span>                                                                             | <span data-ttu-id="a57b6-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="a57b6-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="a57b6-120">**Alteração**</span><span class="sxs-lookup"><span data-stu-id="a57b6-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="a57b6-121">Modifica um serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="a57b6-122">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="a57b6-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="a57b6-123">Modifica o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="a57b6-124">**Criar**</span><span class="sxs-lookup"><span data-stu-id="a57b6-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="a57b6-125">Cria um serviço novo.</span><span class="sxs-lookup"><span data-stu-id="a57b6-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="a57b6-126">**Excluir**</span><span class="sxs-lookup"><span data-stu-id="a57b6-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="a57b6-127">Exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="a57b6-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="a57b6-128">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="a57b6-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="a57b6-129">Solicita que o serviço atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="a57b6-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="a57b6-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="a57b6-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="a57b6-131">Tenta colocar o serviço no estado de pausado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="a57b6-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="a57b6-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="a57b6-133">Tenta colocar o serviço no estado de reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="a57b6-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="a57b6-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="a57b6-135">Tenta posicionar o serviço em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="a57b6-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="a57b6-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a57b6-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="a57b6-137">Método de classe que coloca o serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="a57b6-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="a57b6-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="a57b6-139">Tenta enviar um código de controle definido pelo usuário para um serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="a57b6-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a57b6-140">Properties</span></span>

<span data-ttu-id="a57b6-141">A classe **Win32 \_ BaseService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a57b6-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a57b6-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="a57b6-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a57b6-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-145">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ Pause \_ Continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("o serviço aceita Pause")</span><span class="sxs-lookup"><span data-stu-id="a57b6-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-146">O serviço pode ser pausado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="a57b6-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a57b6-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-150">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| Service \_ Accept \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("o serviço aceita Stop")</span><span class="sxs-lookup"><span data-stu-id="a57b6-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-151">O serviço pode ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="a57b6-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-152">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a57b6-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-155">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a57b6-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-156">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a57b6-156">Short description of the object.</span></span>

<span data-ttu-id="a57b6-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-158">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a57b6-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-161">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="a57b6-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-162">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a57b6-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a57b6-163">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a57b6-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a57b6-164">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-165">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a57b6-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-168">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a57b6-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-169">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a57b6-169">Description of the object.</span></span>

<span data-ttu-id="a57b6-170">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="a57b6-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-172">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a57b6-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-174">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| processo interativo do serviço \_ \_ "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interage com a área de trabalho")</span><span class="sxs-lookup"><span data-stu-id="a57b6-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-175">O serviço pode criar ou se comunicar com o Windows na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a57b6-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-176">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="a57b6-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-179">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta da \| [**\_ \_ configuração do serviço**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome de exibição")</span><span class="sxs-lookup"><span data-stu-id="a57b6-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-180">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-180">Display name of the service.</span></span> <span data-ttu-id="a57b6-181">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a57b6-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="a57b6-182">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="a57b6-183">As comparações de **DisplayName** sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a57b6-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="a57b6-184">Restrições: aceita o mesmo valor que a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="a57b6-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="a57b6-185">Exemplo: "atdisk"</span><span class="sxs-lookup"><span data-stu-id="a57b6-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="a57b6-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-189">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| do serviço de \| [**consulta da \_ \_ configuração do serviço**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("severidade de falha na inicialização")</span><span class="sxs-lookup"><span data-stu-id="a57b6-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-190">Gravidade do erro.</span><span class="sxs-lookup"><span data-stu-id="a57b6-190">Severity of the error.</span></span> <span data-ttu-id="a57b6-191">Falha ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-191">Service fails to start.</span></span> <span data-ttu-id="a57b6-192">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="a57b6-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="a57b6-193">Todos os erros são anotados pelo sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="a57b6-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="a57b6-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("ignorar")</span><span class="sxs-lookup"><span data-stu-id="a57b6-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-195">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="a57b6-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="a57b6-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-197">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="a57b6-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("severo")</span><span class="sxs-lookup"><span data-stu-id="a57b6-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-199">O sistema foi reiniciado com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="a57b6-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="a57b6-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="a57b6-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-201">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="a57b6-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a57b6-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a57b6-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-203">A ação executada não foi especificada.</span><span class="sxs-lookup"><span data-stu-id="a57b6-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a57b6-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="a57b6-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-205">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a57b6-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-207">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de saída")</span><span class="sxs-lookup"><span data-stu-id="a57b6-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-208">Definição de qualquer problema encontrado ao iniciar ou parar o serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="a57b6-209">Essa propriedade é definida como **\_ \_ \_ erro específico do serviço de erro** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="a57b6-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="a57b6-210">O serviço define esse valor como **sem \_ erros** durante a execução e novamente após o término normal.</span><span class="sxs-lookup"><span data-stu-id="a57b6-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a57b6-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-212">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a57b6-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-214">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a57b6-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-215">O objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-215">Object was installed.</span></span> <span data-ttu-id="a57b6-216">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a57b6-217">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-218">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a57b6-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-221">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a57b6-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-222">Identificador exclusivo do serviço, que fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="a57b6-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="a57b6-223">Essa funcionalidade é descrita mais detalhadamente na propriedade **Description** do objeto.</span><span class="sxs-lookup"><span data-stu-id="a57b6-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="a57b6-224">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="a57b6-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-226">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-228">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome do caminho do arquivo")</span><span class="sxs-lookup"><span data-stu-id="a57b6-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-229">Caminho totalmente qualificado para o arquivo binário de serviço que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="a57b6-230">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="a57b6-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-231">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="a57b6-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-232">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a57b6-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-234">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de saída específico do servidor")</span><span class="sxs-lookup"><span data-stu-id="a57b6-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-235">Código de erro específico do serviço para erros que ocorrem enquanto o serviço está sendo iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="a57b6-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="a57b6-236">Os códigos de saída são definidos pelo serviço representado por essa classe.</span><span class="sxs-lookup"><span data-stu-id="a57b6-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="a57b6-237">Esse valor só é definido quando o valor de **ExitCodeproperty** é um **\_ \_ \_ erro específico do serviço de erro** (1066).</span><span class="sxs-lookup"><span data-stu-id="a57b6-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="a57b6-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-239">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-241">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de serviço")</span><span class="sxs-lookup"><span data-stu-id="a57b6-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-242">Serviço fornecido para chamar processos.</span><span class="sxs-lookup"><span data-stu-id="a57b6-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="a57b6-243">**Driver de kernel** ("driver de kernel")</span><span class="sxs-lookup"><span data-stu-id="a57b6-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="a57b6-244">**Driver do sistema de arquivos** ("driver do sistema de arquivos")</span><span class="sxs-lookup"><span data-stu-id="a57b6-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="a57b6-245">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="a57b6-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="a57b6-246">**Driver do reconhecedor** ("driver do reconhecedor")</span><span class="sxs-lookup"><span data-stu-id="a57b6-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="a57b6-247">**Próprio processo** ("processo próprio")</span><span class="sxs-lookup"><span data-stu-id="a57b6-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="a57b6-248">**Processo de compartilhamento** ("processo de compartilhamento")</span><span class="sxs-lookup"><span data-stu-id="a57b6-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="a57b6-249">**Processo interativo** ("processo interativo")</span><span class="sxs-lookup"><span data-stu-id="a57b6-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a57b6-250">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="a57b6-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-251">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a57b6-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-253">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="a57b6-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-254">O serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-254">Service has been started.</span></span>

<span data-ttu-id="a57b6-255">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-256">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="a57b6-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-259">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("startMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="a57b6-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-260">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="a57b6-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="a57b6-261">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="a57b6-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="a57b6-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-263">Driver de dispositivo iniciado pelo carregador do sistema operacional (válido somente para serviços de driver).</span><span class="sxs-lookup"><span data-stu-id="a57b6-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="a57b6-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="a57b6-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-265">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a57b6-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="a57b6-266">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="a57b6-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="a57b6-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automático** ("auto")</span><span class="sxs-lookup"><span data-stu-id="a57b6-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-268">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="a57b6-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="a57b6-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="a57b6-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-270">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a57b6-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a57b6-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="a57b6-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="a57b6-272">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a57b6-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="a57b6-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-276">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da conta inicial")</span><span class="sxs-lookup"><span data-stu-id="a57b6-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-277">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-277">Account name under which the service runs.</span></span> <span data-ttu-id="a57b6-278">Dependendo do tipo de serviço, o nome da conta pode estar na forma de "DomainName \\ username" ou do formato UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="a57b6-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="a57b6-279">O processo de serviço será registrado usando uma dessas duas formas quando for executado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="a57b6-280">Se a conta pertencer ao domínio interno, ". \\ Username "pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="a57b6-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="a57b6-281">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a57b6-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="a57b6-282">Para drivers de nível de kernel ou de sistema, **StartName** contém o nome do objeto de driver (ou seja, \\ FileSystem \\ rdr ou o \\ Driver \\ XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a57b6-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="a57b6-283">Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="a57b6-284">Exemplo: "administrador do DWDOM \\ ".</span><span class="sxs-lookup"><span data-stu-id="a57b6-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-285">**State**</span><span class="sxs-lookup"><span data-stu-id="a57b6-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-287">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a57b6-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-288">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="a57b6-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-289">Estado atual do serviço base.</span><span class="sxs-lookup"><span data-stu-id="a57b6-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="a57b6-290">**Parado** ("parado")</span><span class="sxs-lookup"><span data-stu-id="a57b6-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="a57b6-291">**Início pendente** ("início pendente")</span><span class="sxs-lookup"><span data-stu-id="a57b6-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="a57b6-292">**Parada pendente** ("parar pendente")</span><span class="sxs-lookup"><span data-stu-id="a57b6-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a57b6-293">**Em execução** ("em execução")</span><span class="sxs-lookup"><span data-stu-id="a57b6-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="a57b6-294">**Continuação pendente** ("continuar pendente")</span><span class="sxs-lookup"><span data-stu-id="a57b6-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="a57b6-295">**Pausa pendente** ("pausa pendente")</span><span class="sxs-lookup"><span data-stu-id="a57b6-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a57b6-296">Em **pausa** ("pausado")</span><span class="sxs-lookup"><span data-stu-id="a57b6-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a57b6-297">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a57b6-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="a57b6-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a57b6-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="a57b6-299">**Windows Server 2008 e Windows Vista:** Esta propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a57b6-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-300">**Status**</span><span class="sxs-lookup"><span data-stu-id="a57b6-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-303">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a57b6-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-304">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a57b6-304">Current status of the object.</span></span> <span data-ttu-id="a57b6-305">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a57b6-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a57b6-306">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a57b6-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a57b6-307">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="a57b6-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a57b6-308">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="a57b6-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a57b6-309">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="a57b6-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a57b6-310">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a57b6-311">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a57b6-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a57b6-312">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a57b6-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a57b6-313">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a57b6-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a57b6-314">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a57b6-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a57b6-315">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a57b6-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a57b6-316">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a57b6-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a57b6-317">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a57b6-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a57b6-318">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a57b6-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a57b6-319">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a57b6-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a57b6-320">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a57b6-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a57b6-321">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a57b6-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a57b6-322">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a57b6-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a57b6-323">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a57b6-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a57b6-324">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a57b6-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-327">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="a57b6-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-328">Digite o nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="a57b6-329">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-330">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a57b6-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a57b6-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-333">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="a57b6-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-334">Nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="a57b6-335">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="a57b6-336">**TagId**</span><span class="sxs-lookup"><span data-stu-id="a57b6-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a57b6-337">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a57b6-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a57b6-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a57b6-339">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID da marca")</span><span class="sxs-lookup"><span data-stu-id="a57b6-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="a57b6-340">Valor de marca exclusivo para este serviço no grupo.</span><span class="sxs-lookup"><span data-stu-id="a57b6-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="a57b6-341">Um valor de 0 (zero) indica que não foi atribuída uma marca ao serviço.</span><span class="sxs-lookup"><span data-stu-id="a57b6-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="a57b6-342">Uma marca pode ser usada para ordenar o Service Star scrip em um grupo de ordem de carregamento, especificando um vetor de ordem de marca no Registro localizado em: HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList.</span><span class="sxs-lookup"><span data-stu-id="a57b6-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="a57b6-343">As marcas são avaliadas somente para serviços de inicialização de driver de kernel e driver de sistema de arquivos que têm os modos inicializar ou iniciar sistema.</span><span class="sxs-lookup"><span data-stu-id="a57b6-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a57b6-344">Comentários</span><span class="sxs-lookup"><span data-stu-id="a57b6-344">Remarks</span></span>

<span data-ttu-id="a57b6-345">A classe **Win32 \_ BaseService** é derivada do [**\_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a57b6-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a57b6-346">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a57b6-346">Requirements</span></span>



| <span data-ttu-id="a57b6-347">Requisito</span><span class="sxs-lookup"><span data-stu-id="a57b6-347">Requirement</span></span> | <span data-ttu-id="a57b6-348">Valor</span><span class="sxs-lookup"><span data-stu-id="a57b6-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a57b6-349">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a57b6-349">Minimum supported client</span></span><br/> | <span data-ttu-id="a57b6-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a57b6-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a57b6-351">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a57b6-351">Minimum supported server</span></span><br/> | <span data-ttu-id="a57b6-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a57b6-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a57b6-353">Namespace</span><span class="sxs-lookup"><span data-stu-id="a57b6-353">Namespace</span></span><br/>                | <span data-ttu-id="a57b6-354">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a57b6-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a57b6-355">MOF</span><span class="sxs-lookup"><span data-stu-id="a57b6-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a57b6-356"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a57b6-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a57b6-357">DLL</span><span class="sxs-lookup"><span data-stu-id="a57b6-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a57b6-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a57b6-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a57b6-359">Confira também</span><span class="sxs-lookup"><span data-stu-id="a57b6-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57b6-360">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="a57b6-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="a57b6-361">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a57b6-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

