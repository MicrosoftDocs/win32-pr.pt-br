---
description: Representa o serviço de migração do sistema virtual. Ele é usado para migrar um sistema virtual ou para migrar o armazenamento de um sistema virtual de uma plataforma de virtualização para outra.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646813"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="043bd-104">\_Classe Msvm VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="043bd-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="043bd-105">Representa o serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="043bd-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="043bd-106">Ele é usado para migrar um sistema virtual ou para migrar o armazenamento de um sistema virtual de uma plataforma de virtualização para outra.</span><span class="sxs-lookup"><span data-stu-id="043bd-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="043bd-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="043bd-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="043bd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="043bd-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="043bd-109">Membros</span><span class="sxs-lookup"><span data-stu-id="043bd-109">Members</span></span>

<span data-ttu-id="043bd-110">A classe **Msvm \_ VirtualSystemMigrationService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="043bd-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="043bd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="043bd-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="043bd-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="043bd-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="043bd-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="043bd-113">Methods</span></span>

<span data-ttu-id="043bd-114">A classe **Msvm \_ VirtualSystemMigrationService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="043bd-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="043bd-115">Método</span><span class="sxs-lookup"><span data-stu-id="043bd-115">Method</span></span>                                                                                                                  | <span data-ttu-id="043bd-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="043bd-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="043bd-117">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="043bd-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="043bd-118">Adiciona sub-redes de rede de migração para o serviço de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="043bd-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="043bd-119">**CheckSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="043bd-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="043bd-120">Verifica a compatibilidade das informações de compatibilidade com o sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="043bd-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="043bd-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="043bd-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="043bd-122">Método para migrar um sistema virtual ou o armazenamento de um sistema virtual para um host de destino especificado por um nome de host.</span><span class="sxs-lookup"><span data-stu-id="043bd-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="043bd-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="043bd-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="043bd-124">Determina se o sistema virtual especificado pode ser migrado para um host de destino especificado por um nome de rede ou endereço IP.</span><span class="sxs-lookup"><span data-stu-id="043bd-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="043bd-125">**GetSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="043bd-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="043bd-126">Gera um blob opaco de dados que contém informações de compatibilidade para o sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="043bd-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="043bd-127">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="043bd-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="043bd-128">Obtém vetores de compatibilidade para uma máquina virtual ou um host.</span><span class="sxs-lookup"><span data-stu-id="043bd-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="043bd-129">**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="043bd-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="043bd-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="043bd-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="043bd-131">Migra um sistema virtual ou o armazenamento de um sistema virtual para um host de destino especificado por um nome de host.</span><span class="sxs-lookup"><span data-stu-id="043bd-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="043bd-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="043bd-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="043bd-133">Move, migra ou realoca um sistema virtual para um sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="043bd-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="043bd-134">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="043bd-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="043bd-135">Modifica as sub-redes da rede de migração do serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="043bd-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="043bd-136">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="043bd-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="043bd-137">Modifica os dados de configuração para o serviço de migração.</span><span class="sxs-lookup"><span data-stu-id="043bd-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="043bd-138">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="043bd-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="043bd-139">Remove as sub-redes da rede de migração do serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="043bd-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="043bd-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="043bd-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="043bd-141">Solicita uma alteração de estado</span><span class="sxs-lookup"><span data-stu-id="043bd-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="043bd-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="043bd-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="043bd-143">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="043bd-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="043bd-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="043bd-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="043bd-145">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="043bd-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="043bd-146">Propriedades</span><span class="sxs-lookup"><span data-stu-id="043bd-146">Properties</span></span>

<span data-ttu-id="043bd-147">A classe **Msvm \_ VirtualSystemMigrationService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="043bd-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="043bd-148">**ActiveStorageMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="043bd-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="043bd-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-151">O número de migrações de armazenamento atuais em andamento.</span><span class="sxs-lookup"><span data-stu-id="043bd-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-152">**ActiveVirtualSystemMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="043bd-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="043bd-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-155">O número de migrações de sistema virtual atuais em andamento.</span><span class="sxs-lookup"><span data-stu-id="043bd-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="043bd-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-157">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="043bd-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-159">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="043bd-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="043bd-160">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="043bd-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-161">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="043bd-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-164">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="043bd-164">A short description of the object.</span></span> <span data-ttu-id="043bd-165">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de migração do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="043bd-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-166">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="043bd-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-169">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="043bd-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="043bd-170">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="043bd-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043bd-171">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043bd-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043bd-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-175">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="043bd-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="043bd-176">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ VirtualSystemMigrationService".</span><span class="sxs-lookup"><span data-stu-id="043bd-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-177">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="043bd-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-180">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="043bd-180">A description of the object.</span></span> <span data-ttu-id="043bd-181">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de migração do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="043bd-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="043bd-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-185">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="043bd-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="043bd-186">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="043bd-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043bd-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043bd-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="043bd-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-191">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="043bd-191">A display name for the object.</span></span> <span data-ttu-id="043bd-192">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de migração do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="043bd-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-193">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="043bd-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-194">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-196">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="043bd-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="043bd-197">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="043bd-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="043bd-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-201">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="043bd-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="043bd-202">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="043bd-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="043bd-203">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="043bd-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="043bd-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-205">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-207">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="043bd-207">The current health of the element.</span></span> <span data-ttu-id="043bd-208">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="043bd-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="043bd-209">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="043bd-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="043bd-210">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="043bd-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="043bd-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-212">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="043bd-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-214">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="043bd-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="043bd-215">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043bd-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="043bd-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043bd-219">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="043bd-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="043bd-220">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="043bd-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="043bd-221">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="043bd-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-222">**MigrationServiceListenerIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="043bd-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-223">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="043bd-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-225">A lista de endereços IP de host que podem ser usados para migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="043bd-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-226">**Nome**</span><span class="sxs-lookup"><span data-stu-id="043bd-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-229">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="043bd-229">The label by which the object is known.</span></span> <span data-ttu-id="043bd-230">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "migrationwmi".</span><span class="sxs-lookup"><span data-stu-id="043bd-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-231">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="043bd-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-232">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-234">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="043bd-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="043bd-235">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="043bd-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043bd-236">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043bd-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="043bd-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-238">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="043bd-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-240">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="043bd-240">The current statuses of the object.</span></span> <span data-ttu-id="043bd-241">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="043bd-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-242">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="043bd-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-245">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="043bd-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="043bd-246">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="043bd-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="043bd-247">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="043bd-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="043bd-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-251">Um valor que fornece informações sobre como o proprietário principal do serviço pode ser alcançado (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="043bd-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="043bd-252">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="043bd-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-253">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="043bd-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-254">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-255">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-256">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="043bd-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="043bd-257">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="043bd-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="043bd-258">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="043bd-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-259">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="043bd-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-260">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-262">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="043bd-262">Provides high level status information.</span></span> <span data-ttu-id="043bd-263">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="043bd-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="043bd-264">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="043bd-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="043bd-265">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="043bd-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="043bd-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-267">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-269">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="043bd-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="043bd-270">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="043bd-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="043bd-271">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="043bd-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="043bd-272">Uma determinada instância do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não dar suporte ao método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="043bd-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="043bd-273">Se isso ocorrer, o valor 12 (não aplicável) será usado.</span><span class="sxs-lookup"><span data-stu-id="043bd-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="043bd-274">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="043bd-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-275">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="043bd-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-276">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="043bd-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-278">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="043bd-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="043bd-279">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="043bd-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="043bd-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-283">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="043bd-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="043bd-284">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="043bd-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="043bd-285">**Status**</span><span class="sxs-lookup"><span data-stu-id="043bd-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-286">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="043bd-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-289">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="043bd-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-290">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="043bd-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-292">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="043bd-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="043bd-293">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e as cadeias de caracteres são sempre definidas como "OK".</span><span class="sxs-lookup"><span data-stu-id="043bd-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-294">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043bd-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-297">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="043bd-297">The scoping system's creation class name.</span></span> <span data-ttu-id="043bd-298">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="043bd-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="043bd-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="043bd-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="043bd-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-302">O nome do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="043bd-302">The name of the hosting computer system.</span></span> <span data-ttu-id="043bd-303">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="043bd-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-304">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="043bd-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-305">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="043bd-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-307">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="043bd-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="043bd-308">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="043bd-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="043bd-309">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="043bd-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043bd-310">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043bd-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043bd-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="043bd-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043bd-312">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="043bd-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="043bd-313">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="043bd-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="043bd-314">Requisitos</span><span class="sxs-lookup"><span data-stu-id="043bd-314">Requirements</span></span>



| <span data-ttu-id="043bd-315">Requisito</span><span class="sxs-lookup"><span data-stu-id="043bd-315">Requirement</span></span> | <span data-ttu-id="043bd-316">Valor</span><span class="sxs-lookup"><span data-stu-id="043bd-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="043bd-317">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="043bd-317">Minimum supported client</span></span><br/> | <span data-ttu-id="043bd-318">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="043bd-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="043bd-319">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="043bd-319">Minimum supported server</span></span><br/> | <span data-ttu-id="043bd-320">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="043bd-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="043bd-321">Namespace</span><span class="sxs-lookup"><span data-stu-id="043bd-321">Namespace</span></span><br/>                | <span data-ttu-id="043bd-322">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="043bd-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="043bd-323">MOF</span><span class="sxs-lookup"><span data-stu-id="043bd-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="043bd-324"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="043bd-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="043bd-325">DLL</span><span class="sxs-lookup"><span data-stu-id="043bd-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="043bd-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="043bd-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

