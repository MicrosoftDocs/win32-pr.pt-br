---
description: Define o meio pelo qual um cliente pode descobrir o intervalo válido de configurações padrão para um recurso virtual.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Classe Msvm_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810354"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="39a39-103">\_Classe Msvm AllocationCapabilities</span><span class="sxs-lookup"><span data-stu-id="39a39-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="39a39-104">Define o meio pelo qual um cliente pode descobrir o intervalo válido de configurações padrão para um recurso virtual.</span><span class="sxs-lookup"><span data-stu-id="39a39-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="39a39-105">Um objeto **Msvm \_ AllocationCapabilities** está associado a cada pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="39a39-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="39a39-106">Quatro objetos [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) são associados ao objeto **Msvm \_ AllocationCapabilities** para descrever os valores mínimo, máximo, padrão e incremental para a alocação do recurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="39a39-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="39a39-107">Juntas, essas classes descrevem o intervalo geral de recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="39a39-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="39a39-108">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="39a39-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a39-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39a39-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="39a39-110">Membros</span><span class="sxs-lookup"><span data-stu-id="39a39-110">Members</span></span>

<span data-ttu-id="39a39-111">A classe **Msvm \_ AllocationCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39a39-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="39a39-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39a39-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39a39-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39a39-113">Properties</span></span>

<span data-ttu-id="39a39-114">A classe **Msvm \_ AllocationCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39a39-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39a39-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="39a39-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39a39-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39a39-118">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="39a39-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="39a39-119">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="39a39-119">A short description of the object.</span></span> <span data-ttu-id="39a39-120">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="39a39-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39a39-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39a39-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39a39-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-124">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="39a39-124">A description of the object.</span></span> <span data-ttu-id="39a39-125">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="39a39-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39a39-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="39a39-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39a39-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-129">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="39a39-129">A display name for the object.</span></span> <span data-ttu-id="39a39-130">Essa propriedade permite que cada instância defina um nome de exibição além de suas propriedades de chave, dados de identidade e informações de descrição.</span><span class="sxs-lookup"><span data-stu-id="39a39-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="39a39-131">A propriedade [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) da classe **CIM \_ ManagedSystemElement** também é definida como um nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="39a39-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="39a39-132">Mas, muitas vezes, é uma subclasse para ser uma chave.</span><span class="sxs-lookup"><span data-stu-id="39a39-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="39a39-133">Não é razoável que a mesma propriedade possa transmitir a identidade e um nome de exibição, sem inconsistências.</span><span class="sxs-lookup"><span data-stu-id="39a39-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="39a39-134">Quando o [**nome**](msvm-keyboard.md) existe e não é uma chave (como para instâncias de um dispositivo lógico), as mesmas informações podem estar presentes nas propriedades **Name** e **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="39a39-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="39a39-135">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="39a39-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39a39-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39a39-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39a39-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-139">Um identificador exclusivo para este pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="39a39-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="39a39-140">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="39a39-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39a39-141">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="39a39-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39a39-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-144">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor "other".</span><span class="sxs-lookup"><span data-stu-id="39a39-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="39a39-145">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="39a39-146">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="39a39-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39a39-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-149">Indica se há suporte para a solicitação de um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="39a39-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="39a39-150">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="39a39-151">Valor</span><span class="sxs-lookup"><span data-stu-id="39a39-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="39a39-152">Significado</span><span class="sxs-lookup"><span data-stu-id="39a39-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="39a39-153"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="39a39-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="39a39-154">Unknown</span><span class="sxs-lookup"><span data-stu-id="39a39-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="39a39-155"><dt>**Específico**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="39a39-156">A solicitação pode incluir uma solicitação para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="39a39-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="39a39-157"><dt>**Geral**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="39a39-158">A solicitação não inclui uma solicitação para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="39a39-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="39a39-159"><dt>**Ambos**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="39a39-160">Há suporte para solicitações específicas e gerais.</span><span class="sxs-lookup"><span data-stu-id="39a39-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="39a39-161">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="39a39-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39a39-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-164">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="39a39-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="39a39-165">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="39a39-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="39a39-166">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="39a39-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="39a39-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39a39-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-170">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="39a39-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="39a39-171">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="39a39-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="39a39-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="39a39-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="39a39-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="39a39-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="39a39-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="39a39-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="39a39-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="39a39-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="39a39-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="39a39-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="39a39-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="39a39-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="39a39-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="39a39-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="39a39-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="39a39-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="39a39-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="39a39-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="39a39-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="39a39-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="39a39-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="39a39-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="39a39-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="39a39-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="39a39-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="39a39-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="39a39-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energia** (28)</span><span class="sxs-lookup"><span data-stu-id="39a39-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacidade de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="39a39-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="39a39-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="39a39-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="39a39-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="39a39-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39a39-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="39a39-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39a39-207">**Sharingmode**</span><span class="sxs-lookup"><span data-stu-id="39a39-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-208">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39a39-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39a39-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-210">Indica como o acesso a um recurso subjacente é concedido.</span><span class="sxs-lookup"><span data-stu-id="39a39-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="39a39-211">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="39a39-212">Valor</span><span class="sxs-lookup"><span data-stu-id="39a39-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="39a39-213">Significado</span><span class="sxs-lookup"><span data-stu-id="39a39-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="39a39-214"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="39a39-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="39a39-215">Unknown</span><span class="sxs-lookup"><span data-stu-id="39a39-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="39a39-216"><dt>**Dedicado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="39a39-217">Acesso exclusivo a um recurso subjacente.</span><span class="sxs-lookup"><span data-stu-id="39a39-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="39a39-218"><dt>**Compartilhado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="39a39-219">Uso compartilhado de um recurso subjacente.</span><span class="sxs-lookup"><span data-stu-id="39a39-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="39a39-220">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="39a39-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-221">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39a39-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39a39-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-223">Indica os Estados em que o sistema ao qual o recurso será associado pode estar quando um novo recurso é criado.</span><span class="sxs-lookup"><span data-stu-id="39a39-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="39a39-224">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="39a39-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="39a39-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="39a39-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="39a39-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (4)</span><span class="sxs-lookup"><span data-stu-id="39a39-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="39a39-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="39a39-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (7)</span><span class="sxs-lookup"><span data-stu-id="39a39-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="39a39-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="39a39-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (10)</span><span class="sxs-lookup"><span data-stu-id="39a39-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="39a39-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (12)</span><span class="sxs-lookup"><span data-stu-id="39a39-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39a39-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="39a39-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39a39-239">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="39a39-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39a39-240">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39a39-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39a39-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39a39-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39a39-242">Indica os Estados em que o sistema ao qual o recurso está associado pode estar quando o recurso é removido.</span><span class="sxs-lookup"><span data-stu-id="39a39-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="39a39-243">Essa propriedade é herdada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="39a39-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="39a39-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="39a39-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="39a39-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="39a39-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (4)</span><span class="sxs-lookup"><span data-stu-id="39a39-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="39a39-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="39a39-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (7)</span><span class="sxs-lookup"><span data-stu-id="39a39-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="39a39-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="39a39-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (10)</span><span class="sxs-lookup"><span data-stu-id="39a39-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="39a39-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (12)</span><span class="sxs-lookup"><span data-stu-id="39a39-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39a39-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39a39-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="39a39-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39a39-258">Comentários</span><span class="sxs-lookup"><span data-stu-id="39a39-258">Remarks</span></span>

<span data-ttu-id="39a39-259">O acesso à classe **Msvm \_ AllocationCapabilities** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="39a39-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="39a39-260">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="39a39-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="39a39-261">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39a39-261">Requirements</span></span>



| <span data-ttu-id="39a39-262">Requisito</span><span class="sxs-lookup"><span data-stu-id="39a39-262">Requirement</span></span> | <span data-ttu-id="39a39-263">Valor</span><span class="sxs-lookup"><span data-stu-id="39a39-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a39-264">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39a39-264">Minimum supported client</span></span><br/> | <span data-ttu-id="39a39-265">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="39a39-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39a39-266">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39a39-266">Minimum supported server</span></span><br/> | <span data-ttu-id="39a39-267">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="39a39-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39a39-268">Namespace</span><span class="sxs-lookup"><span data-stu-id="39a39-268">Namespace</span></span><br/>                | <span data-ttu-id="39a39-269">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="39a39-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39a39-270">MOF</span><span class="sxs-lookup"><span data-stu-id="39a39-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39a39-271"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39a39-272">DLL</span><span class="sxs-lookup"><span data-stu-id="39a39-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39a39-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39a39-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39a39-274">Confira também</span><span class="sxs-lookup"><span data-stu-id="39a39-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a39-275">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="39a39-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="39a39-276">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="39a39-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="39a39-277">**Msvm \_ AllocationCapabilities (v1)**</span><span class="sxs-lookup"><span data-stu-id="39a39-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="39a39-278">Classes de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="39a39-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

