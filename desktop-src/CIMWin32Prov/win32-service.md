---
description: Representa um serviço em um sistema de computador que executa o Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Classe Win32_Service
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010113"
---
# <a name="win32_service-class"></a><span data-ttu-id="e91a6-103">\_Classe de serviço Win32</span><span class="sxs-lookup"><span data-stu-id="e91a6-103">Win32\_Service class</span></span>

<span data-ttu-id="e91a6-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ serviço do Win32** representa um serviço em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="e91a6-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="e91a6-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e91a6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e91a6-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="e91a6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e91a6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="e91a6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e91a6-108">Members</span></span>

<span data-ttu-id="e91a6-109">A classe de **\_ serviço do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e91a6-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="e91a6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e91a6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e91a6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e91a6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e91a6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e91a6-112">Methods</span></span>

<span data-ttu-id="e91a6-113">A classe de **\_ serviço do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e91a6-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="e91a6-114">Método</span><span class="sxs-lookup"><span data-stu-id="e91a6-114">Method</span></span>                                                                               | <span data-ttu-id="e91a6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e91a6-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e91a6-116">**Alteração**</span><span class="sxs-lookup"><span data-stu-id="e91a6-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="e91a6-117">Modifica um serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="e91a6-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="e91a6-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="e91a6-119">Modifica o modo de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="e91a6-120">**Criar**</span><span class="sxs-lookup"><span data-stu-id="e91a6-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="e91a6-121">Cria um serviço novo.</span><span class="sxs-lookup"><span data-stu-id="e91a6-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="e91a6-122">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="e91a6-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="e91a6-123">Exclui um serviço existente.</span><span class="sxs-lookup"><span data-stu-id="e91a6-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="e91a6-124">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e91a6-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="e91a6-125">Retorna o descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="e91a6-126">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="e91a6-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="e91a6-127">Solicita que um serviço atualize seu estado para o Service Manager.</span><span class="sxs-lookup"><span data-stu-id="e91a6-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="e91a6-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="e91a6-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="e91a6-129">Tenta colocar um serviço no estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="e91a6-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="e91a6-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="e91a6-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="e91a6-131">Tenta posicionar um serviço no estado retomado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="e91a6-132">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e91a6-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="e91a6-133">Grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="e91a6-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="e91a6-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="e91a6-135">Tenta posicionar um serviço no estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e91a6-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="e91a6-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="e91a6-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="e91a6-137">Coloca um serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="e91a6-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="e91a6-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="e91a6-139">Tenta enviar um código de controle definido pelo usuário para um serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="e91a6-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e91a6-140">Properties</span></span>

<span data-ttu-id="e91a6-141">A classe de **\_ serviço do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e91a6-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e91a6-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="e91a6-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e91a6-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-145">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ Pause \_ Continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("o serviço aceita Pause")</span><span class="sxs-lookup"><span data-stu-id="e91a6-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-146">Indica se o serviço pode ser pausado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="e91a6-147">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="e91a6-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-149">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e91a6-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-151">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| Service \_ Accept \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("o serviço aceita Stop")</span><span class="sxs-lookup"><span data-stu-id="e91a6-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-152">Indica se o serviço pode ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="e91a6-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="e91a6-153">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-154">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e91a6-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-157">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e91a6-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-158">Breve descrição do serviço — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="e91a6-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="e91a6-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-160">**Verifica**</span><span class="sxs-lookup"><span data-stu-id="e91a6-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-163">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de pontos de verificação")</span><span class="sxs-lookup"><span data-stu-id="e91a6-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-164">Valor que o serviço incrementa periodicamente para relatar seu progresso durante uma longa operação de início, parada, pausa ou continuação.</span><span class="sxs-lookup"><span data-stu-id="e91a6-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="e91a6-165">Por exemplo, o serviço incrementa esse valor à medida que ele conclui cada etapa de sua inicialização quando ele está sendo inicializado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="e91a6-166">O programa de interface do usuário que invoca a operação no serviço usa esse valor para acompanhar o progresso do serviço durante uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="e91a6-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="e91a6-167">Esse valor não é válido e deve ser zero quando o serviço não tem uma operação de início, parada, pausa ou continuação pendente.</span><span class="sxs-lookup"><span data-stu-id="e91a6-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-168">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e91a6-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-171">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="e91a6-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-172">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e91a6-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e91a6-173">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e91a6-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e91a6-174">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="e91a6-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-176">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e91a6-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-178">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("as \| estruturas de serviço win32api \| [**serviço de \_ \_ início automático atrasado de \_ \_ informações**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("início automático atrasado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-179">Se **for true**, o serviço será iniciado depois que outros serviços de início automático forem iniciados além de um pequeno atraso.</span><span class="sxs-lookup"><span data-stu-id="e91a6-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="e91a6-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e91a6-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-181">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e91a6-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-184">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e91a6-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-185">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="e91a6-185">Description of the object.</span></span>

<span data-ttu-id="e91a6-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="e91a6-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-188">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e91a6-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-190">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| processo interativo do serviço \_ \_ "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("interage com a área de trabalho")</span><span class="sxs-lookup"><span data-stu-id="e91a6-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-191">Indica se o serviço pode criar ou se comunicar com o Windows na área de trabalho e, portanto, interagir de alguma maneira com um usuário.</span><span class="sxs-lookup"><span data-stu-id="e91a6-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="e91a6-192">Os serviços interativos devem ser executados na conta sistema local.</span><span class="sxs-lookup"><span data-stu-id="e91a6-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="e91a6-193">A maioria dos serviços não são interativos; ou seja, eles não se comunicam com o usuário de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="e91a6-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="e91a6-194">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-195">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="e91a6-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-198">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta da \| [**\_ \_ configuração do serviço**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome de exibição")</span><span class="sxs-lookup"><span data-stu-id="e91a6-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-199">Nome do serviço como exibido no snap-in serviços.</span><span class="sxs-lookup"><span data-stu-id="e91a6-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="e91a6-200">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e91a6-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="e91a6-201">Observe que o nome de exibição e o nome do serviço (que é armazenado no registro) nem sempre são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="e91a6-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="e91a6-202">Por exemplo, o serviço de cliente DHCP tem o nome de serviço DHCP, mas o nome de exibição cliente DHCP.</span><span class="sxs-lookup"><span data-stu-id="e91a6-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="e91a6-203">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="e91a6-204">No entanto, as comparações **DisplayName** sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e91a6-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="e91a6-205">Restrição: aceita o mesmo valor que a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="e91a6-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="e91a6-206">Exemplo: "atdisk"</span><span class="sxs-lookup"><span data-stu-id="e91a6-206">Example: "Atdisk"</span></span>

<span data-ttu-id="e91a6-207">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="e91a6-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-211">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| do serviço de \| [**consulta da \_ \_ configuração do serviço**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("severidade de falha na inicialização")</span><span class="sxs-lookup"><span data-stu-id="e91a6-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-212">Severidade do erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="e91a6-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="e91a6-213">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="e91a6-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="e91a6-214">Todos os erros são anotados pelo sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="e91a6-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="e91a6-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("ignorar")</span><span class="sxs-lookup"><span data-stu-id="e91a6-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-216">O usuário não é notificado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="e91a6-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")</span><span class="sxs-lookup"><span data-stu-id="e91a6-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-218">O usuário é notificado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-218">User is notified.</span></span> <span data-ttu-id="e91a6-219">Normalmente, essa será uma caixa de mensagem exibida notificando o usuário do problema.</span><span class="sxs-lookup"><span data-stu-id="e91a6-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="e91a6-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("severo")</span><span class="sxs-lookup"><span data-stu-id="e91a6-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-221">Sistema é reiniciado com a última configuração bem-sucedida conhecida.</span><span class="sxs-lookup"><span data-stu-id="e91a6-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="e91a6-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")</span><span class="sxs-lookup"><span data-stu-id="e91a6-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-223">O sistema tenta reiniciar com uma configuração adequada.</span><span class="sxs-lookup"><span data-stu-id="e91a6-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="e91a6-224">Se o serviço não for iniciado pela segunda vez, a inicialização falhará.</span><span class="sxs-lookup"><span data-stu-id="e91a6-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e91a6-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e91a6-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-226">A severidade do erro é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="e91a6-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="e91a6-227">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-228">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="e91a6-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-229">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-231">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("código de saída")</span><span class="sxs-lookup"><span data-stu-id="e91a6-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-232">Código de erro do Windows que define os erros encontrados ao iniciar ou interromper o serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="e91a6-233">Essa propriedade é definida como **\_ \_ \_ erro específico do serviço de erro** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="e91a6-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="e91a6-234">O serviço define esse valor como **sem \_ erros** durante a execução e novamente após o término normal.</span><span class="sxs-lookup"><span data-stu-id="e91a6-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="e91a6-235">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e91a6-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-237">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e91a6-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-239">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e91a6-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-240">O objeto de data está instalado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-240">Date object is installed.</span></span> <span data-ttu-id="e91a6-241">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e91a6-242">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-243">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e91a6-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-246">Qualificadores: [ **chave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="e91a6-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-247">Identificador exclusivo do serviço que fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e91a6-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="e91a6-248">Essa funcionalidade é descrita na propriedade **Descrição** do objeto.</span><span class="sxs-lookup"><span data-stu-id="e91a6-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="e91a6-249">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="e91a6-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-251">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-252">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-253">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome do caminho do arquivo")</span><span class="sxs-lookup"><span data-stu-id="e91a6-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-254">Caminho totalmente qualificado para o arquivo binário de serviço que implementa o serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="e91a6-255">Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="e91a6-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="e91a6-256">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-257">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="e91a6-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-258">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-259">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-260">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| código de status do serviço de estruturas de serviço win32api \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| DwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID do processo")</span><span class="sxs-lookup"><span data-stu-id="e91a6-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-261">Identificador do processo do serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-261">Process identifier of the service.</span></span>

<span data-ttu-id="e91a6-262">Exemplo: 324</span><span class="sxs-lookup"><span data-stu-id="e91a6-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-263">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="e91a6-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-264">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-266">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("código de saída específico do servidor")</span><span class="sxs-lookup"><span data-stu-id="e91a6-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-267">Código de erro específico do serviço para erros que ocorrem enquanto o serviço está sendo iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="e91a6-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="e91a6-268">Os códigos de saída são definidos pelo serviço representado por essa classe.</span><span class="sxs-lookup"><span data-stu-id="e91a6-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="e91a6-269">Esse valor só é definido quando o valor da propriedade **ExitCode** é um **\_ \_ \_ erro específico do serviço de erro** (1066).</span><span class="sxs-lookup"><span data-stu-id="e91a6-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="e91a6-270">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="e91a6-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-274">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo de serviço")</span><span class="sxs-lookup"><span data-stu-id="e91a6-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-275">Tipo de serviço fornecido a processos de chamada.</span><span class="sxs-lookup"><span data-stu-id="e91a6-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="e91a6-276">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e91a6-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="e91a6-277">**Driver de kernel** ("driver de kernel")</span><span class="sxs-lookup"><span data-stu-id="e91a6-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="e91a6-278">**Driver do sistema de arquivos** ("driver do sistema de arquivos")</span><span class="sxs-lookup"><span data-stu-id="e91a6-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="e91a6-279">**Adaptador** ("adaptador")</span><span class="sxs-lookup"><span data-stu-id="e91a6-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="e91a6-280">**Driver do reconhecedor** ("driver do reconhecedor")</span><span class="sxs-lookup"><span data-stu-id="e91a6-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="e91a6-281">**Próprio processo** ("processo próprio")</span><span class="sxs-lookup"><span data-stu-id="e91a6-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="e91a6-282">**Processo de compartilhamento** ("processo de compartilhamento")</span><span class="sxs-lookup"><span data-stu-id="e91a6-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="e91a6-283">**Processo interativo** ("processo interativo")</span><span class="sxs-lookup"><span data-stu-id="e91a6-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="e91a6-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e91a6-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="e91a6-285">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-286">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="e91a6-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-287">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e91a6-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-289">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-290">Indica se o serviço é iniciado ou não.</span><span class="sxs-lookup"><span data-stu-id="e91a6-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="e91a6-291">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-292">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="e91a6-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-295">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="e91a6-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-296">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="e91a6-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="e91a6-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização** ("inicialização")</span><span class="sxs-lookup"><span data-stu-id="e91a6-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-298">Driver de dispositivo iniciado pelo carregador do sistema operacional (válido somente para serviços de driver).</span><span class="sxs-lookup"><span data-stu-id="e91a6-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="e91a6-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")</span><span class="sxs-lookup"><span data-stu-id="e91a6-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-300">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e91a6-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="e91a6-301">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="e91a6-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="e91a6-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automático** ("auto")</span><span class="sxs-lookup"><span data-stu-id="e91a6-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-303">Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="e91a6-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="e91a6-304">Os serviços automáticos são iniciados mesmo se um usuário não fizer logon.</span><span class="sxs-lookup"><span data-stu-id="e91a6-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="e91a6-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="e91a6-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-306">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="e91a6-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="e91a6-307">Esses serviços não são iniciados, a menos que um usuário faça logon e os inicie.</span><span class="sxs-lookup"><span data-stu-id="e91a6-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e91a6-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="e91a6-309">Serviço que não pode ser iniciado até que seu StartMode seja alterado para automático ou manual.</span><span class="sxs-lookup"><span data-stu-id="e91a6-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="e91a6-310">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="e91a6-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-314">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da conta inicial")</span><span class="sxs-lookup"><span data-stu-id="e91a6-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-315">Nome da conta sob a qual um serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-315">Account name under which a service runs.</span></span> <span data-ttu-id="e91a6-316">Dependendo do tipo de serviço, o nome da conta pode estar na forma de "DomainName \\ username" ou do formato UPN (" *Username@DomainName* ").</span><span class="sxs-lookup"><span data-stu-id="e91a6-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="e91a6-317">O processo de serviço é registrado usando uma dessas duas formas quando é executado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="e91a6-318">Se a conta pertencer ao domínio interno, então ". \\ Username "pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="e91a6-319">Para drivers de nível de kernel ou de sistema, o **StartName** contém o nome do objeto de driver (ou seja, " \\ FileSystem \\ rdr" ou " \\ Driver \\ XNS") que o sistema de e/s usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e91a6-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="e91a6-320">Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="e91a6-321">Exemplo: "administrador do DWDOM \\ "</span><span class="sxs-lookup"><span data-stu-id="e91a6-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="e91a6-322">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-323">**State**</span><span class="sxs-lookup"><span data-stu-id="e91a6-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-325">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e91a6-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-326">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="e91a6-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-327">Estado atual do serviço base.</span><span class="sxs-lookup"><span data-stu-id="e91a6-327">Current state of the base service.</span></span>

<span data-ttu-id="e91a6-328">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e91a6-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="e91a6-329">**Parado** ("parado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="e91a6-330">**Início pendente** ("início pendente")</span><span class="sxs-lookup"><span data-stu-id="e91a6-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="e91a6-331">**Parada pendente** ("parar pendente")</span><span class="sxs-lookup"><span data-stu-id="e91a6-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="e91a6-332">**Em execução** ("em execução")</span><span class="sxs-lookup"><span data-stu-id="e91a6-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="e91a6-333">**Continuação pendente** ("continuar pendente")</span><span class="sxs-lookup"><span data-stu-id="e91a6-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="e91a6-334">**Pausa pendente** ("pausa pendente")</span><span class="sxs-lookup"><span data-stu-id="e91a6-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e91a6-335">Em **pausa** ("pausado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e91a6-336">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e91a6-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="e91a6-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e91a6-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="e91a6-338">**Windows Server 2008 e Windows Vista:** Essa propriedade é somente leitura antes do Windows 7 e do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e91a6-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="e91a6-339">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-340">**Status**</span><span class="sxs-lookup"><span data-stu-id="e91a6-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-343">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="e91a6-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-344">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e91a6-344">Current status of the object.</span></span> <span data-ttu-id="e91a6-345">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="e91a6-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e91a6-346">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="e91a6-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e91a6-347">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e91a6-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e91a6-348">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e91a6-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e91a6-349">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e91a6-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e91a6-350">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e91a6-351">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e91a6-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e91a6-352">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e91a6-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e91a6-353">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e91a6-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e91a6-354">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e91a6-355">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e91a6-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e91a6-356">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e91a6-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e91a6-357">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e91a6-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e91a6-358">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e91a6-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e91a6-359">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e91a6-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e91a6-360">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e91a6-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e91a6-361">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e91a6-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e91a6-362">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e91a6-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e91a6-363">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e91a6-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e91a6-364">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e91a6-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-367">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="e91a6-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-368">Digite o nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="e91a6-369">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-370">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e91a6-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-371">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e91a6-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-373">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="e91a6-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-374">Nome do sistema que hospeda este serviço.</span><span class="sxs-lookup"><span data-stu-id="e91a6-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="e91a6-375">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-376">**TagId**</span><span class="sxs-lookup"><span data-stu-id="e91a6-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-377">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-379">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID da marca")</span><span class="sxs-lookup"><span data-stu-id="e91a6-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-380">Valor de marca exclusivo para este serviço no grupo.</span><span class="sxs-lookup"><span data-stu-id="e91a6-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="e91a6-381">Um valor de 0 (zero) indica que o serviço não tem uma marca.</span><span class="sxs-lookup"><span data-stu-id="e91a6-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="e91a6-382">Uma marca pode ser usada para ordenar a inicialização do serviço dentro de um grupo de ordem de carregamento, especificando um vetor de ordem de marca no Registro localizado em:</span><span class="sxs-lookup"><span data-stu-id="e91a6-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="e91a6-383">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **GroupOrderList**    </span><span class="sxs-lookup"><span data-stu-id="e91a6-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="e91a6-384">As marcas são avaliadas somente para os serviços de tipo de inicialização driver de kernel e driver de sistema de arquivos que têm os modos de inicialização do sistema ou inicializados.</span><span class="sxs-lookup"><span data-stu-id="e91a6-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="e91a6-385">Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e91a6-386">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="e91a6-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e91a6-387">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e91a6-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e91a6-389">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tempo de espera estimado")</span><span class="sxs-lookup"><span data-stu-id="e91a6-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="e91a6-390">Tempo estimado necessário, em milissegundos, para uma operação de início, parada, pausa ou continuação pendente.</span><span class="sxs-lookup"><span data-stu-id="e91a6-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="e91a6-391">Depois que o tempo especificado tiver decorrido, o serviço fará sua próxima chamada para o método **falha em SetServiceStatus** com um valor de **ponto de verificação** incrementado ou uma alteração no **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="e91a6-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="e91a6-392">Se o tempo especificado por **WaitHint** passa e o ponto de **verificação** não tiver sido incrementado ou **CurrentState** não tiver sido alterado, o Gerenciador de controle de serviço ou o programa de controle de serviço assumirá que ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="e91a6-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e91a6-393">Comentários</span><span class="sxs-lookup"><span data-stu-id="e91a6-393">Remarks</span></span>

<span data-ttu-id="e91a6-394">A classe de **\_ serviço do Win32** é derivada do [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="e91a6-395">A maneira como você gerencia um computador específico depende muito da função que o computador desempenha.</span><span class="sxs-lookup"><span data-stu-id="e91a6-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="e91a6-396">Por exemplo, você geralmente monitora diferentes aspectos de um servidor DNS do que um servidor DHCP.</span><span class="sxs-lookup"><span data-stu-id="e91a6-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="e91a6-397">Embora nenhuma única propriedade possa informar se um computador específico é um servidor de banco de dados, um servidor de email ou um servidor de multimídia, geralmente é possível identificar a função que um computador desempenha identificando os serviços instalados nele.</span><span class="sxs-lookup"><span data-stu-id="e91a6-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="e91a6-398">Em grandes organizações, é provável que apenas um dos principais serviços (como email) seja instalado em um único computador.</span><span class="sxs-lookup"><span data-stu-id="e91a6-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="e91a6-399">Seria incomum que um servidor de email também fosse executado como um servidor para os arquivos de player do Microsoft® Windows Media® Technologies.</span><span class="sxs-lookup"><span data-stu-id="e91a6-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="e91a6-400">Por isso, a identificação de um serviço instalado em um computador pode ajudar a identificar a função do computador na rede.</span><span class="sxs-lookup"><span data-stu-id="e91a6-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="e91a6-401">Se o serviço do Microsoft® Exchange Server estiver instalado e em execução em um computador, geralmente é seguro supor que esse computador funciona como um servidor de email.</span><span class="sxs-lookup"><span data-stu-id="e91a6-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="e91a6-402">Você pode usar a classe **de \_ serviço WMI Win32** para enumerar os serviços instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="e91a6-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="e91a6-403">Além disso, você pode usar essa classe para determinar se esses serviços estão em execução no momento e para retornar outras informações necessárias sobre esse serviço e como ele foi configurado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="e91a6-404">Um aplicativo de serviço está em conformidade com as regras de interface do SCM (Gerenciador de controle de serviço) e pode ser iniciado por um usuário automaticamente na inicialização do sistema por meio do utilitário do painel de controle de serviços ou por um aplicativo que usa as funções de serviço incluídas na API do Windows.</span><span class="sxs-lookup"><span data-stu-id="e91a6-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="e91a6-405">Os serviços podem ser iniciados quando não há usuários conectados ao computador.</span><span class="sxs-lookup"><span data-stu-id="e91a6-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="e91a6-406">Um usuário que se conecta a partir de um computador remoto deve ter o privilégio do **sc \_ Manager \_ Connect** habilitado para poder enumerar essa classe.</span><span class="sxs-lookup"><span data-stu-id="e91a6-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="e91a6-407">Para obter mais informações, consulte [segurança de serviço e direitos de acesso](../services/service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="e91a6-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e91a6-408">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e91a6-408">Examples</span></span>

<span data-ttu-id="e91a6-409">A [consulta PS-WMI que retorna o serviço ' estado ' em um grupo de dispositivos](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) exemplo do PowerShell na galeria do TechNet usa o **\_ serviço Win32** para criar uma lista de dispositivos de Active Directory e, em seguida, consultar cada dispositivo que responde com pingfor um serviço específico em execução.</span><span class="sxs-lookup"><span data-stu-id="e91a6-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="e91a6-410">A amostra do PowerShell de [relatório do servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) na galeria do TechNet usa o **\_ serviço Win32** para coletar informações do servidor e publicar no documento do Word.</span><span class="sxs-lookup"><span data-stu-id="e91a6-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="e91a6-411">O exemplo de código VBScript a seguir exibe todos os serviços instalados no momento.</span><span class="sxs-lookup"><span data-stu-id="e91a6-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="e91a6-412">O exemplo de código VBScript a seguir descreve os serviços em pausa, em execução e parado no computador especificado.</span><span class="sxs-lookup"><span data-stu-id="e91a6-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="e91a6-413">O script Perl a seguir demonstra como recuperar uma lista de serviços em execução de instâncias **do \_ serviço Win32**.</span><span class="sxs-lookup"><span data-stu-id="e91a6-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="e91a6-414">O exemplo c a seguir \# usa [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar todos os serviços em execução no computador local.</span><span class="sxs-lookup"><span data-stu-id="e91a6-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="e91a6-415">O exemplo de código C a seguir \# usa o namespace [System. Management](/dotnet/api/system.management) para recuperar todos os serviços em execução no computador local.</span><span class="sxs-lookup"><span data-stu-id="e91a6-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="e91a6-416">[System. Management](/dotnet/api/system.management) contém as classes originais usadas para acessar o WMI; no entanto, eles são considerados mais lentos e geralmente não são dimensionados, bem como seus equivalentes de [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e91a6-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="e91a6-417">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e91a6-417">Requirements</span></span>



| <span data-ttu-id="e91a6-418">Requisito</span><span class="sxs-lookup"><span data-stu-id="e91a6-418">Requirement</span></span> | <span data-ttu-id="e91a6-419">Valor</span><span class="sxs-lookup"><span data-stu-id="e91a6-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e91a6-420">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e91a6-420">Minimum supported client</span></span><br/> | <span data-ttu-id="e91a6-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e91a6-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e91a6-422">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e91a6-422">Minimum supported server</span></span><br/> | <span data-ttu-id="e91a6-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e91a6-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e91a6-424">Namespace</span><span class="sxs-lookup"><span data-stu-id="e91a6-424">Namespace</span></span><br/>                | <span data-ttu-id="e91a6-425">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e91a6-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e91a6-426">MOF</span><span class="sxs-lookup"><span data-stu-id="e91a6-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e91a6-427"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e91a6-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e91a6-428">DLL</span><span class="sxs-lookup"><span data-stu-id="e91a6-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e91a6-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e91a6-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e91a6-430">Confira também</span><span class="sxs-lookup"><span data-stu-id="e91a6-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91a6-431">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="e91a6-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="e91a6-432">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="e91a6-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e91a6-433">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="e91a6-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
