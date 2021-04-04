---
description: Representa o driver do sistema para um serviço base.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646375"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="6974e-103">Classe de SystemDrive do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="6974e-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="6974e-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) da **\_ systemdrive do Win32** representa o driver do sistema para um serviço base.</span><span class="sxs-lookup"><span data-stu-id="6974e-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="6974e-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6974e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6974e-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="6974e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6974e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6974e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="6974e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6974e-108">Members</span></span>

<span data-ttu-id="6974e-109">A **classe \_ systemdrive do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6974e-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="6974e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6974e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6974e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6974e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6974e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6974e-112">Methods</span></span>

<span data-ttu-id="6974e-113">A **classe \_ systemdrive do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6974e-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="6974e-114">Método</span><span class="sxs-lookup"><span data-stu-id="6974e-114">Method</span></span>                                                                              | <span data-ttu-id="6974e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6974e-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6974e-116">**Alteração**</span><span class="sxs-lookup"><span data-stu-id="6974e-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="6974e-117">Método de classe que modifica um serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="6974e-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="6974e-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="6974e-119">Método de classe que modifica o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="6974e-120">**Criar**</span><span class="sxs-lookup"><span data-stu-id="6974e-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="6974e-121">Método de classe que cria um novo serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="6974e-122">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="6974e-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="6974e-123">Método de classe que exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="6974e-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="6974e-124">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="6974e-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="6974e-125">Método de classe que solicita que o serviço atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="6974e-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="6974e-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="6974e-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="6974e-127">Método de classe que tenta colocar o serviço no estado pausado.</span><span class="sxs-lookup"><span data-stu-id="6974e-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="6974e-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="6974e-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="6974e-129">Método de classe que tenta posicionar o serviço no estado retomado.</span><span class="sxs-lookup"><span data-stu-id="6974e-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="6974e-130">**StartService**</span><span class="sxs-lookup"><span data-stu-id="6974e-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="6974e-131">Método de classe que tenta posicionar o serviço em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="6974e-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="6974e-132">**StopService**</span><span class="sxs-lookup"><span data-stu-id="6974e-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="6974e-133">Método de classe que coloca o serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="6974e-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="6974e-134">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="6974e-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="6974e-135">Método de classe que tenta enviar um código de controle definido pelo usuário para um serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="6974e-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6974e-136">Properties</span></span>

<span data-ttu-id="6974e-137">A **classe \_ systemdrive do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6974e-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6974e-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="6974e-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6974e-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-141">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ Pause \_ Continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("o serviço aceita Pause")</span><span class="sxs-lookup"><span data-stu-id="6974e-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-142">O serviço pode ser pausado.</span><span class="sxs-lookup"><span data-stu-id="6974e-142">Service can be paused.</span></span>

<span data-ttu-id="6974e-143">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="6974e-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6974e-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-147">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| Service \_ Accept \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("o serviço aceita Stop")</span><span class="sxs-lookup"><span data-stu-id="6974e-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-148">O serviço pode ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="6974e-148">Service can be stopped.</span></span>

<span data-ttu-id="6974e-149">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-150">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6974e-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-153">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6974e-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-154">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6974e-154">Short description of the object.</span></span>

<span data-ttu-id="6974e-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6974e-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-159">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="6974e-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-160">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="6974e-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6974e-161">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="6974e-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6974e-162">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-163">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6974e-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-166">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="6974e-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-167">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6974e-167">Description of the object.</span></span>

<span data-ttu-id="6974e-168">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="6974e-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6974e-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-172">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| processo interativo do serviço \_ \_ "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("interage com a área de trabalho")</span><span class="sxs-lookup"><span data-stu-id="6974e-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-173">Esse serviço pode criar ou se comunicar com o Windows na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6974e-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="6974e-174">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-175">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6974e-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-178">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta da \| [**\_ \_ configuração do serviço**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome de exibição")</span><span class="sxs-lookup"><span data-stu-id="6974e-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-179">Nome de exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-179">Display name of the service.</span></span> <span data-ttu-id="6974e-180">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6974e-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="6974e-181">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="6974e-182">As comparações **DisplayName** sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6974e-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="6974e-183">Restrições: aceita o mesmo valor que a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="6974e-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="6974e-184">Exemplo: "atdisk"</span><span class="sxs-lookup"><span data-stu-id="6974e-184">Example: "Atdisk"</span></span>

<span data-ttu-id="6974e-185">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="6974e-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-189">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| do serviço de \| [**consulta da \_ \_ configuração do serviço**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("severidade de falha na inicialização")</span><span class="sxs-lookup"><span data-stu-id="6974e-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-190">Severidade do erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="6974e-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="6974e-191">Esse valor indica a ação realizada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="6974e-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="6974e-192">Todos os erros são anotados pelo sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="6974e-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="6974e-193">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="6974e-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("ignorar")</span><span class="sxs-lookup"><span data-stu-id="6974e-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-195">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="6974e-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="6974e-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="6974e-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-197">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="6974e-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="6974e-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("severo")</span><span class="sxs-lookup"><span data-stu-id="6974e-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-199">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="6974e-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="6974e-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="6974e-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-201">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="6974e-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6974e-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6974e-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-203">A causa da falha é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="6974e-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6974e-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="6974e-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-205">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6974e-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-207">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("código de saída")</span><span class="sxs-lookup"><span data-stu-id="6974e-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-208">Código de erro do Windows que define os problemas encontrados ao iniciar ou interromper o serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="6974e-209">Essa propriedade é definida como **\_ \_ \_ erro específico do serviço de erro** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="6974e-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="6974e-210">O serviço define esse valor como **sem \_ erros** durante a execução e novamente após o término normal.</span><span class="sxs-lookup"><span data-stu-id="6974e-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="6974e-211">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6974e-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-213">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6974e-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-215">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="6974e-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-216">O objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6974e-216">Object was installed.</span></span> <span data-ttu-id="6974e-217">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="6974e-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6974e-218">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-219">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6974e-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-222">Qualificadores: [ **chave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6974e-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="6974e-223">Identificador exclusivo do serviço que fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="6974e-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="6974e-224">Essa funcionalidade é descrita mais detalhadamente na propriedade **Descrição** do objeto.</span><span class="sxs-lookup"><span data-stu-id="6974e-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="6974e-225">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="6974e-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-229">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome do caminho do arquivo")</span><span class="sxs-lookup"><span data-stu-id="6974e-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-230">Caminho totalmente qualificado para o arquivo binário de serviço que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="6974e-231">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="6974e-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="6974e-232">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-233">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="6974e-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-234">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6974e-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-235">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-236">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("código de saída específico do servidor")</span><span class="sxs-lookup"><span data-stu-id="6974e-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-237">Código de erro específico do serviço para erros que ocorrem enquanto o serviço está sendo iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="6974e-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="6974e-238">Os códigos de saída são definidos pelo serviço representado por essa classe.</span><span class="sxs-lookup"><span data-stu-id="6974e-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="6974e-239">Esse valor só é definido quando o valor da propriedade **ExitCode** é um **\_ \_ \_ erro específico do serviço de erro** (1066).</span><span class="sxs-lookup"><span data-stu-id="6974e-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="6974e-240">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="6974e-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-244">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo de serviço")</span><span class="sxs-lookup"><span data-stu-id="6974e-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-245">Tipo de serviço fornecido a processos de chamada.</span><span class="sxs-lookup"><span data-stu-id="6974e-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="6974e-246">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="6974e-247">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="6974e-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="6974e-248">**Driver de kernel** ("driver de kernel")</span><span class="sxs-lookup"><span data-stu-id="6974e-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="6974e-249">**Driver do sistema de arquivos** ("driver do sistema de arquivos")</span><span class="sxs-lookup"><span data-stu-id="6974e-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="6974e-250">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="6974e-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="6974e-251">**Driver do reconhecedor** ("driver do reconhecedor")</span><span class="sxs-lookup"><span data-stu-id="6974e-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="6974e-252">**Próprio processo** ("processo próprio")</span><span class="sxs-lookup"><span data-stu-id="6974e-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="6974e-253">**Processo de compartilhamento** ("processo de compartilhamento")</span><span class="sxs-lookup"><span data-stu-id="6974e-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="6974e-254">**Processo interativo** ("processo interativo")</span><span class="sxs-lookup"><span data-stu-id="6974e-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6974e-255">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="6974e-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-256">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6974e-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-258">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="6974e-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-259">O serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="6974e-259">Service has been started.</span></span>

<span data-ttu-id="6974e-260">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-261">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="6974e-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-264">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="6974e-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-265">Modo de início do driver do sistema.</span><span class="sxs-lookup"><span data-stu-id="6974e-265">Start mode of the system driver.</span></span>

<span data-ttu-id="6974e-266">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="6974e-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="6974e-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-268">Driver de dispositivo iniciado pelo carregador do sistema operacional (válido somente para serviços de driver).</span><span class="sxs-lookup"><span data-stu-id="6974e-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="6974e-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="6974e-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-270">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6974e-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="6974e-271">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="6974e-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="6974e-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automático** ("auto")</span><span class="sxs-lookup"><span data-stu-id="6974e-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-273">Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="6974e-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="6974e-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="6974e-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-275">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="6974e-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6974e-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="6974e-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="6974e-277">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="6974e-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6974e-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="6974e-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-281">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da conta inicial")</span><span class="sxs-lookup"><span data-stu-id="6974e-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-282">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="6974e-282">Account name under which the service runs.</span></span> <span data-ttu-id="6974e-283">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome_do_domínio \\ username.</span><span class="sxs-lookup"><span data-stu-id="6974e-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="6974e-284">O processo de serviço será registrado usando uma dessas duas formas quando for executado.</span><span class="sxs-lookup"><span data-stu-id="6974e-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="6974e-285">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="6974e-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="6974e-286">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="6974e-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="6974e-287">Para drivers de nível de kernel ou de sistema, **StartName** contém o nome do objeto de driver (ou seja, \\ FileSystem \\ rdr ou o \\ Driver \\ XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6974e-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="6974e-288">Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="6974e-289">Exemplo: "administrador do DWDOM \\ "</span><span class="sxs-lookup"><span data-stu-id="6974e-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="6974e-290">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-291">**State**</span><span class="sxs-lookup"><span data-stu-id="6974e-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-293">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6974e-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6974e-294">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="6974e-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-295">Estado atual do serviço base.</span><span class="sxs-lookup"><span data-stu-id="6974e-295">Current state of the base service.</span></span>

<span data-ttu-id="6974e-296">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="6974e-297">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="6974e-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="6974e-298">**Parado** ("parado")</span><span class="sxs-lookup"><span data-stu-id="6974e-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="6974e-299">**Início pendente** ("início pendente")</span><span class="sxs-lookup"><span data-stu-id="6974e-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="6974e-300">**Parada pendente** ("parar pendente")</span><span class="sxs-lookup"><span data-stu-id="6974e-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="6974e-301">**Em execução** ("em execução")</span><span class="sxs-lookup"><span data-stu-id="6974e-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="6974e-302">**Continuação pendente** ("continuar pendente")</span><span class="sxs-lookup"><span data-stu-id="6974e-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="6974e-303">**Pausa pendente** ("pausa pendente")</span><span class="sxs-lookup"><span data-stu-id="6974e-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6974e-304">Em **pausa** ("pausado")</span><span class="sxs-lookup"><span data-stu-id="6974e-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6974e-305">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6974e-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6974e-306">**Status**</span><span class="sxs-lookup"><span data-stu-id="6974e-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-309">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="6974e-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-310">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6974e-310">Current status of the object.</span></span> <span data-ttu-id="6974e-311">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="6974e-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6974e-312">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6974e-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6974e-313">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6974e-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6974e-314">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6974e-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6974e-315">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6974e-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6974e-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6974e-317">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="6974e-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6974e-318">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6974e-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6974e-319">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="6974e-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6974e-320">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6974e-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6974e-321">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6974e-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6974e-322">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6974e-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6974e-323">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6974e-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6974e-324">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="6974e-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6974e-325">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="6974e-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6974e-326">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="6974e-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6974e-327">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6974e-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6974e-328">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="6974e-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6974e-329">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="6974e-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6974e-330">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6974e-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-333">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="6974e-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-334">Digite o nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="6974e-335">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-336">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6974e-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6974e-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-339">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="6974e-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-340">Nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="6974e-341">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="6974e-342">**TagId**</span><span class="sxs-lookup"><span data-stu-id="6974e-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6974e-343">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6974e-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6974e-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6974e-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6974e-345">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID da marca")</span><span class="sxs-lookup"><span data-stu-id="6974e-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="6974e-346">Valor de marca exclusivo para este serviço no grupo.</span><span class="sxs-lookup"><span data-stu-id="6974e-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="6974e-347">Um valor de 0 (zero) indica que não foi atribuída uma marca ao serviço.</span><span class="sxs-lookup"><span data-stu-id="6974e-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="6974e-348">Uma marca pode ser usada para ordenar a inicialização do serviço dentro de um grupo de ordem de carregamento, especificando um vetor de ordem de marca no Registro localizado em:</span><span class="sxs-lookup"><span data-stu-id="6974e-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="6974e-349">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="6974e-350">**HKEY \_ O \_ sistema de computador local \\ \\ CurrentControlSet \\ Control \\ GroupOrderList**.</span><span class="sxs-lookup"><span data-stu-id="6974e-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="6974e-351">As marcas são avaliadas somente para serviços de inicialização de driver de kernel e driver de sistema de arquivos que têm os modos inicializar ou iniciar sistema.</span><span class="sxs-lookup"><span data-stu-id="6974e-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6974e-352">Comentários</span><span class="sxs-lookup"><span data-stu-id="6974e-352">Remarks</span></span>

<span data-ttu-id="6974e-353">A classe do **\_ systemdrive do Win32** é derivada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="6974e-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6974e-354">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6974e-354">Examples</span></span>

<span data-ttu-id="6974e-355">O exemplo [listar](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) exemplos de VBScript de drivers do sistema exibe os drivers de sistema instalados em um arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="6974e-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="6974e-356">O exemplo do PowerShell a seguir recupera várias propriedades dos drivers do sistema em execução em um computador.</span><span class="sxs-lookup"><span data-stu-id="6974e-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="6974e-357">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6974e-357">Requirements</span></span>



| <span data-ttu-id="6974e-358">Requisito</span><span class="sxs-lookup"><span data-stu-id="6974e-358">Requirement</span></span> | <span data-ttu-id="6974e-359">Valor</span><span class="sxs-lookup"><span data-stu-id="6974e-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6974e-360">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6974e-360">Minimum supported client</span></span><br/> | <span data-ttu-id="6974e-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6974e-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6974e-362">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6974e-362">Minimum supported server</span></span><br/> | <span data-ttu-id="6974e-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6974e-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6974e-364">Namespace</span><span class="sxs-lookup"><span data-stu-id="6974e-364">Namespace</span></span><br/>                | <span data-ttu-id="6974e-365">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6974e-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6974e-366">MOF</span><span class="sxs-lookup"><span data-stu-id="6974e-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6974e-367"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6974e-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6974e-368">DLL</span><span class="sxs-lookup"><span data-stu-id="6974e-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6974e-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6974e-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6974e-370">Confira também</span><span class="sxs-lookup"><span data-stu-id="6974e-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6974e-371">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="6974e-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="6974e-372">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6974e-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
