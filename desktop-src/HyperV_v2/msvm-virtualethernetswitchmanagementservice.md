---
description: Representa o serviço de virtualização presente em um único sistema de host. Msvm \_ VirtualEthernetSwitchManagementService é usado para controlar a definição, modificação e exclusão de comutadores Ethernet virtuais.
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782805"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="1ba57-104">\_Classe Msvm VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="1ba57-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="1ba57-105">Representa o serviço de virtualização presente em um único sistema de host.</span><span class="sxs-lookup"><span data-stu-id="1ba57-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="1ba57-106">Msvm \_ VirtualEthernetSwitchManagementService é usado para controlar a definição, modificação e exclusão de comutadores Ethernet virtuais.</span><span class="sxs-lookup"><span data-stu-id="1ba57-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="1ba57-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1ba57-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba57-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ba57-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="1ba57-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1ba57-109">Members</span></span>

<span data-ttu-id="1ba57-110">A classe **Msvm \_ VirtualEthernetSwitchManagementService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1ba57-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="1ba57-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ba57-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ba57-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ba57-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ba57-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ba57-113">Methods</span></span>

<span data-ttu-id="1ba57-114">A classe **Msvm \_ VirtualEthernetSwitchManagementService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1ba57-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="1ba57-115">Método</span><span class="sxs-lookup"><span data-stu-id="1ba57-115">Method</span></span>                                                                                               | <span data-ttu-id="1ba57-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ba57-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="1ba57-117">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="1ba57-118">Adiciona configurações de recurso à configuração de uma porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1ba57-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="1ba57-119">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="1ba57-120">Adiciona recursos a uma configuração de comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1ba57-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="1ba57-121">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="1ba57-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="1ba57-122">Cria um novo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1ba57-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="1ba57-123">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="1ba57-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="1ba57-124">Destrói um comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1ba57-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="1ba57-125">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="1ba57-126">Modifica as configurações de recurso de uma porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1ba57-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="1ba57-127">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="1ba57-128">Modifica as configurações de recurso para um comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1ba57-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="1ba57-129">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="1ba57-130">Modifica as configurações do comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1ba57-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="1ba57-131">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="1ba57-132">Remove as configurações de recurso de uma porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="1ba57-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="1ba57-133">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1ba57-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="1ba57-134">Remove as configurações de recurso virtual de uma configuração de comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="1ba57-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="1ba57-135">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1ba57-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="1ba57-136">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="1ba57-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="1ba57-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1ba57-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="1ba57-138">Inicia o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ba57-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="1ba57-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1ba57-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="1ba57-140">Interrompe o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ba57-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="1ba57-141">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ba57-141">Properties</span></span>

<span data-ttu-id="1ba57-142">A classe **Msvm \_ VirtualEthernetSwitchManagementService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1ba57-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ba57-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1ba57-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-144">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-146">Indica os valores possíveis para o parâmetro *requestedstate* do método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="1ba57-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1ba57-147">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-148">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1ba57-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-151">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1ba57-151">A short description of the object.</span></span> <span data-ttu-id="1ba57-152">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de rede virtual do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="1ba57-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-153">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1ba57-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-154">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-156">Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente.</span><span class="sxs-lookup"><span data-stu-id="1ba57-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1ba57-157">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1ba57-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ba57-158">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1ba57-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ba57-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1ba57-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1ba57-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicação Ok** (2)</span><span class="sxs-lookup"><span data-stu-id="1ba57-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="1ba57-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nenhum contato** (4)</span><span class="sxs-lookup"><span data-stu-id="1ba57-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1ba57-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1ba57-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ba57-166">)</span><span class="sxs-lookup"><span data-stu-id="1ba57-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba57-167">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ba57-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-170">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1ba57-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-171">O nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1ba57-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1ba57-172">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ VirtualEthernetSwitchManagementService".</span><span class="sxs-lookup"><span data-stu-id="1ba57-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-173">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1ba57-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-176">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="1ba57-176">A description of the object.</span></span> <span data-ttu-id="1ba57-177">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "fornece gerenciamento WMI de rede do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="1ba57-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1ba57-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-179">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-181">Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais.</span><span class="sxs-lookup"><span data-stu-id="1ba57-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1ba57-182">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1ba57-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ba57-183">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1ba57-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ba57-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (0)</span><span class="sxs-lookup"><span data-stu-id="1ba57-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nenhuma informação adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="1ba57-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sob estresse** (2)</span><span class="sxs-lookup"><span data-stu-id="1ba57-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Falha preditiva** (3)</span><span class="sxs-lookup"><span data-stu-id="1ba57-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erro não recuperável** (4)</span><span class="sxs-lookup"><span data-stu-id="1ba57-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidade de suporte com erro** (5)</span><span class="sxs-lookup"><span data-stu-id="1ba57-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1ba57-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1ba57-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ba57-192">)</span><span class="sxs-lookup"><span data-stu-id="1ba57-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba57-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1ba57-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-196">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1ba57-196">A display name for the object.</span></span> <span data-ttu-id="1ba57-197">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "serviço de gerenciamento de rede do Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="1ba57-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1ba57-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-201">A configuração de inicialização ou padrão de um administrador para o estado habilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1ba57-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="1ba57-202">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="1ba57-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="1ba57-203">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba57-203">Value</span></span>                                                                        | <span data-ttu-id="1ba57-204">Significado</span><span class="sxs-lookup"><span data-stu-id="1ba57-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="1ba57-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ba57-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1ba57-206">habilitado</span><span class="sxs-lookup"><span data-stu-id="1ba57-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ba57-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1ba57-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-210">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="1ba57-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1ba57-211">Essa propriedade também pode indicar as transições entre esses Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="1ba57-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="1ba57-212">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como 5 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="1ba57-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1ba57-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-214">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-216">A integridade atual do elemento.</span><span class="sxs-lookup"><span data-stu-id="1ba57-216">The current health of the element.</span></span> <span data-ttu-id="1ba57-217">Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1ba57-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="1ba57-218">Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional.</span><span class="sxs-lookup"><span data-stu-id="1ba57-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="1ba57-219">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="1ba57-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="1ba57-220">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba57-220">Value</span></span>                                                                        | <span data-ttu-id="1ba57-221">Significado</span><span class="sxs-lookup"><span data-stu-id="1ba57-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="1ba57-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1ba57-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="1ba57-223">O status de integridade é normal.</span><span class="sxs-lookup"><span data-stu-id="1ba57-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ba57-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1ba57-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-225">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1ba57-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-227">A data e a hora em que a configuração da máquina virtual foi criada.</span><span class="sxs-lookup"><span data-stu-id="1ba57-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="1ba57-228">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1ba57-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ba57-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-230">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-232">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="1ba57-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-233">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="1ba57-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1ba57-234">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="1ba57-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-235">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1ba57-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-238">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1ba57-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-239">O rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="1ba57-239">The label by which the object is known.</span></span> <span data-ttu-id="1ba57-240">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "VMMS".</span><span class="sxs-lookup"><span data-stu-id="1ba57-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-241">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1ba57-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-242">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-244">Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da propriedade **enabledstate** .</span><span class="sxs-lookup"><span data-stu-id="1ba57-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1ba57-245">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1ba57-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ba57-246">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1ba57-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ba57-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1ba57-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Não disponível** (1)</span><span class="sxs-lookup"><span data-stu-id="1ba57-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenção** (2)</span><span class="sxs-lookup"><span data-stu-id="1ba57-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)</span><span class="sxs-lookup"><span data-stu-id="1ba57-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Parando** (4)</span><span class="sxs-lookup"><span data-stu-id="1ba57-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (5)</span><span class="sxs-lookup"><span data-stu-id="1ba57-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="1ba57-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inativo** (7)</span><span class="sxs-lookup"><span data-stu-id="1ba57-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (8)</span><span class="sxs-lookup"><span data-stu-id="1ba57-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrando** (9)</span><span class="sxs-lookup"><span data-stu-id="1ba57-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="1ba57-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span><span class="sxs-lookup"><span data-stu-id="1ba57-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantâneo** (12)</span><span class="sxs-lookup"><span data-stu-id="1ba57-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (13)</span><span class="sxs-lookup"><span data-stu-id="1ba57-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (14)</span><span class="sxs-lookup"><span data-stu-id="1ba57-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição** (15)</span><span class="sxs-lookup"><span data-stu-id="1ba57-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Em serviço** (16)</span><span class="sxs-lookup"><span data-stu-id="1ba57-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1ba57-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1ba57-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ba57-266">)</span><span class="sxs-lookup"><span data-stu-id="1ba57-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba57-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1ba57-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-268">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-270">Os status atuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="1ba57-270">The current statuses of the object.</span></span> <span data-ttu-id="1ba57-271">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="1ba57-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-272">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1ba57-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-273">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-275">Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="1ba57-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="1ba57-276">Essa propriedade deve ser definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.</span><span class="sxs-lookup"><span data-stu-id="1ba57-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1ba57-277">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-278">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="1ba57-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-281">Qualificadores: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1ba57-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-282">Todas as informações sobre como o proprietário principal do serviço podem ser atingidas (por exemplo, número de telefone, endereço de email e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1ba57-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="1ba57-283">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-284">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="1ba57-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-287">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1ba57-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-288">O nome do proprietário principal do serviço, se um estiver definido.</span><span class="sxs-lookup"><span data-stu-id="1ba57-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="1ba57-289">O proprietário principal é o contato de suporte inicial para o serviço.</span><span class="sxs-lookup"><span data-stu-id="1ba57-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="1ba57-290">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-291">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1ba57-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-292">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-294">Fornece informações de status de alto nível.</span><span class="sxs-lookup"><span data-stu-id="1ba57-294">Provides high level status information.</span></span> <span data-ttu-id="1ba57-295">Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer o status de integridade de alto nível e detalhado do elemento e seus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="1ba57-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1ba57-296">Um valor **nulo** indica que essa propriedade não está implementada.</span><span class="sxs-lookup"><span data-stu-id="1ba57-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1ba57-297">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="1ba57-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1ba57-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1ba57-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1ba57-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="1ba57-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (3)</span><span class="sxs-lookup"><span data-stu-id="1ba57-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1ba57-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="1ba57-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1ba57-304">)</span><span class="sxs-lookup"><span data-stu-id="1ba57-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba57-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1ba57-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-306">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-308">O último estado solicitado ou desejado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="1ba57-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="1ba57-309">O estado real do elemento é representado por **enabledstate**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="1ba57-310">Essa propriedade é fornecida para comparar os últimos Estados solicitados e atuais para um elemento.</span><span class="sxs-lookup"><span data-stu-id="1ba57-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="1ba57-311">Uma instância específica da classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) pode não oferecer suporte à propriedade **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="1ba57-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="1ba57-312">Se isso ocorrer, o valor 12 ("não aplicável") será usado.</span><span class="sxs-lookup"><span data-stu-id="1ba57-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="1ba57-313">Essa propriedade é herdada do **CIM \_ EnabledLogicalElement** e é sempre definida como 12 (não aplicável).</span><span class="sxs-lookup"><span data-stu-id="1ba57-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="1ba57-314">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba57-314">Value</span></span>                                                                         | <span data-ttu-id="1ba57-315">Significado</span><span class="sxs-lookup"><span data-stu-id="1ba57-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="1ba57-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1ba57-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1ba57-317">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="1ba57-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1ba57-318">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="1ba57-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-319">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1ba57-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-321">Indica se o serviço está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="1ba57-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="1ba57-322">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-323">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="1ba57-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-326">Qualificadores: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="1ba57-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-327">Um valor de cadeia de caracteres que indica se o serviço é iniciado automaticamente por um sistema, um sistema operacional ou é iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="1ba57-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="1ba57-328">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-329">**Status**</span><span class="sxs-lookup"><span data-stu-id="1ba57-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-332">Descreve o status atual do serviço.</span><span class="sxs-lookup"><span data-stu-id="1ba57-332">Describes the current status of the service.</span></span> <span data-ttu-id="1ba57-333">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como "OK".</span><span class="sxs-lookup"><span data-stu-id="1ba57-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-334">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1ba57-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-335">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-337">Cadeias de caracteres que descrevem os vários valores de matriz de **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="1ba57-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1ba57-338">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento da matriz é sempre definido como "OK".</span><span class="sxs-lookup"><span data-stu-id="1ba57-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-339">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ba57-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-342">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1ba57-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-343">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1ba57-343">The scoping system's creation class name.</span></span> <span data-ttu-id="1ba57-344">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)e é sempre definida como "Msvm \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="1ba57-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-345">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1ba57-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1ba57-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-348">Qualificadores: **chave**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1ba57-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-349">O nome NetBIOS do sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="1ba57-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="1ba57-350">Essa propriedade é herdada [**do \_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="1ba57-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-351">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1ba57-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-352">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1ba57-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-354">A data ou a hora em que o estado habilitado do elemento foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="1ba57-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1ba57-355">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ba57-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1ba57-356">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1ba57-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba57-357">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba57-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba57-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1ba57-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba57-359">Indica o estado de destino para o qual a instância está em transição.</span><span class="sxs-lookup"><span data-stu-id="1ba57-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1ba57-360">Essa propriedade é herdada do [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e é sempre definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ba57-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ba57-361">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba57-361">Requirements</span></span>



| <span data-ttu-id="1ba57-362">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba57-362">Requirement</span></span> | <span data-ttu-id="1ba57-363">Valor</span><span class="sxs-lookup"><span data-stu-id="1ba57-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba57-364">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ba57-364">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba57-365">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ba57-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ba57-366">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ba57-366">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba57-367">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ba57-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ba57-368">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ba57-368">Namespace</span></span><br/>                | <span data-ttu-id="1ba57-369">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="1ba57-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ba57-370">MOF</span><span class="sxs-lookup"><span data-stu-id="1ba57-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ba57-371"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ba57-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ba57-372">DLL</span><span class="sxs-lookup"><span data-stu-id="1ba57-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ba57-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ba57-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

