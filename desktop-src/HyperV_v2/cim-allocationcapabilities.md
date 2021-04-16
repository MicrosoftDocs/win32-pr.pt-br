---
description: Representa as configurações de alocação de recursos de um elemento gerenciado para um tipo de recurso específico.
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: Classe CIM_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758991"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="3a5fd-103">\_Classe CIM AllocationCapabilities</span><span class="sxs-lookup"><span data-stu-id="3a5fd-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="3a5fd-104">Representa as configurações de alocação de recursos de um elemento gerenciado para um tipo de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5fd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a5fd-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="3a5fd-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3a5fd-106">Members</span></span>

<span data-ttu-id="3a5fd-107">A classe **CIM \_ AllocationCapabilities** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3a5fd-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="3a5fd-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a5fd-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a5fd-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a5fd-109">Properties</span></span>

<span data-ttu-id="3a5fd-110">A classe **CIM \_ AllocationCapabilities** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a5fd-111">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="3a5fd-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-115">O tipo de recurso para essa configuração de alocação quando a propriedade **ResourceType** é definida como "1" (outra).</span><span class="sxs-lookup"><span data-stu-id="3a5fd-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="3a5fd-116">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-119">Indica se há suporte para a solicitação de um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a5fd-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="3a5fd-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Específico** (2)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a5fd-122">A solicitação pode incluir uma solicitação de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="3a5fd-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**Geral** (3)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a5fd-124">A solicitação não inclui um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="3a5fd-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Ambos** (4)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3a5fd-126">Há suporte para solicitações específicas e gerais.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a5fd-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a5fd-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3a5fd-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a5fd-129">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-132">Uma descrição de um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="3a5fd-133">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="3a5fd-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-137">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AllocationCapabilities**.**OtherResourceType**","[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="3a5fd-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-138">O tipo de recurso atribuído a essa configuração de alocação.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a5fd-139">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="3a5fd-140">**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="3a5fd-141">**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="3a5fd-142">**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="3a5fd-143">**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="3a5fd-144">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="3a5fd-145">**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="3a5fd-146">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="3a5fd-147">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="3a5fd-148">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="3a5fd-149">**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="3a5fd-150">**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="3a5fd-151">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="3a5fd-152">**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="3a5fd-153">**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="3a5fd-154">**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="3a5fd-155">**Unidade de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="3a5fd-156">**Unidade de fita** (18)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="3a5fd-157">**Extensão de armazenamento** (19)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="3a5fd-158">**Outro dispositivo de armazenamento** (20)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="3a5fd-159">**Porta serial** (21)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="3a5fd-160">**Porta paralela** (22)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="3a5fd-161">**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="3a5fd-162">**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="3a5fd-163">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="3a5fd-164">**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="3a5fd-165">**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="3a5fd-166">**Energia** (28)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="3a5fd-167">**Capacidade de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="3a5fd-168">**Porta do comutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="3a5fd-169">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="3a5fd-170">**Volume de armazenamento** (32)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="3a5fd-171">**Conexão Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a5fd-172">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a5fd-173">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3a5fd-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a5fd-174">**Sharingmode**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-175">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-177">Indica como o acesso ao recurso subjacente é concedido.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="3a5fd-178">A quantidade real é controlada por mín., tamanho máximo, pesos, etc.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a5fd-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="3a5fd-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (2)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a5fd-181">Acesso exclusivo ao recurso subjacente.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="3a5fd-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Compartilhado** (3)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a5fd-183">Uso compartilhado do recurso subjacente.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a5fd-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a5fd-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3a5fd-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a5fd-186">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-187">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-189">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="3a5fd-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-190">O sistema declara que tem suporte quando um novo recurso é criado.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a5fd-191">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3a5fd-192">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3a5fd-193">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="3a5fd-194">**Desligando** (4)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3a5fd-195">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="3a5fd-196">**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3a5fd-197">**Em teste** (7)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="3a5fd-198">**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="3a5fd-199">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a5fd-200">**Iniciando** (10)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3a5fd-201">Em **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="3a5fd-202">**Suspenso** (12)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a5fd-203">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a5fd-204">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3a5fd-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a5fd-205">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a5fd-206">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3a5fd-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a5fd-208">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="3a5fd-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="3a5fd-209">Os Estados do sistema têm suporte quando um recurso é removido.</span><span class="sxs-lookup"><span data-stu-id="3a5fd-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a5fd-210">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3a5fd-211">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3a5fd-212">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="3a5fd-213">**Desligando** (4)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3a5fd-214">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="3a5fd-215">**Habilitado, mas offline** (6)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3a5fd-216">**Em teste** (7)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="3a5fd-217">**Adiado** (8)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="3a5fd-218">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a5fd-219">**Iniciando** (10)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3a5fd-220">Em **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="3a5fd-221">**Suspenso** (12)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3a5fd-222">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3a5fd-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3a5fd-223">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="3a5fd-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="3a5fd-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3a5fd-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="3a5fd-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a5fd-225">Requirements</span></span>



| <span data-ttu-id="3a5fd-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a5fd-226">Requirement</span></span> | <span data-ttu-id="3a5fd-227">Valor</span><span class="sxs-lookup"><span data-stu-id="3a5fd-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5fd-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a5fd-228">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5fd-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a5fd-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3a5fd-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a5fd-230">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5fd-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a5fd-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3a5fd-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a5fd-232">Namespace</span></span><br/>                | <span data-ttu-id="3a5fd-233">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3a5fd-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3a5fd-234">MOF</span><span class="sxs-lookup"><span data-stu-id="3a5fd-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a5fd-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a5fd-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a5fd-236">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5fd-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5fd-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a5fd-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a5fd-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a5fd-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5fd-239">**Recursos de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3a5fd-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

