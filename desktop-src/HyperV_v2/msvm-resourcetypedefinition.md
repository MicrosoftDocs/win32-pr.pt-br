---
description: Define um mapeamento de um tipo de recurso para suas classes de implementação.
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Classe Msvm_ResourceTypeDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789799"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="f0701-103">\_Classe Msvm ResourceTypeDefinition</span><span class="sxs-lookup"><span data-stu-id="f0701-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="f0701-104">Define um mapeamento de um tipo de recurso para suas classes de implementação.</span><span class="sxs-lookup"><span data-stu-id="f0701-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="f0701-105">A sintaxe a seguir é simplificada formato MOF código (MOF).</span><span class="sxs-lookup"><span data-stu-id="f0701-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0701-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0701-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="f0701-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f0701-107">Members</span></span>

<span data-ttu-id="f0701-108">A classe **Msvm \_ ResourceTypeDefinition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f0701-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="f0701-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f0701-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0701-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f0701-110">Properties</span></span>

<span data-ttu-id="f0701-111">A classe **Msvm \_ ResourceTypeDefinition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f0701-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0701-112">**LogicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="f0701-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0701-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f0701-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0701-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f0701-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0701-115">O nome da classe derivada do [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que implementa o dispositivo lógico para esse tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0701-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="f0701-116">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="f0701-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0701-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f0701-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0701-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f0701-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0701-119">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="f0701-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f0701-120">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e **ResourceType** tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="f0701-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="f0701-121">Há uma correspondência com a propriedade **OtherResourceType** do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="f0701-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="f0701-122">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="f0701-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0701-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f0701-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0701-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f0701-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0701-125">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="f0701-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f0701-126">Uma cadeia de caracteres que descreve um subtipo específico de implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f0701-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="f0701-127">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0701-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="f0701-128">Há uma correspondência com a propriedade **ResourceSubType** do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="f0701-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="f0701-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="f0701-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0701-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0701-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0701-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f0701-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0701-132">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="f0701-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f0701-133">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="f0701-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="f0701-134">Há uma correspondência com a propriedade **ResourceType** do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="f0701-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="f0701-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="f0701-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema de computador** (2)</span><span class="sxs-lookup"><span data-stu-id="f0701-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processador** (3)</span><span class="sxs-lookup"><span data-stu-id="f0701-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memória** (4)</span><span class="sxs-lookup"><span data-stu-id="f0701-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="f0701-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="f0701-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="f0701-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="f0701-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="f0701-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="f0701-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Outro adaptador de rede** (11)</span><span class="sxs-lookup"><span data-stu-id="f0701-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="f0701-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="f0701-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidade de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="f0701-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidade de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="f0701-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidade de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="f0701-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta serial** (17)</span><span class="sxs-lookup"><span data-stu-id="f0701-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta paralela** (18)</span><span class="sxs-lookup"><span data-stu-id="f0701-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (19)</span><span class="sxs-lookup"><span data-stu-id="f0701-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (20)</span><span class="sxs-lookup"><span data-stu-id="f0701-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensão de armazenamento** (21)</span><span class="sxs-lookup"><span data-stu-id="f0701-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="f0701-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Fita** (23)</span><span class="sxs-lookup"><span data-stu-id="f0701-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Outro dispositivo de armazenamento** (24)</span><span class="sxs-lookup"><span data-stu-id="f0701-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="f0701-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidade particionável** (26)</span><span class="sxs-lookup"><span data-stu-id="f0701-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidade particionável de base** (27)</span><span class="sxs-lookup"><span data-stu-id="f0701-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fonte de energia** (28)</span><span class="sxs-lookup"><span data-stu-id="f0701-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de resfriamento** (29)</span><span class="sxs-lookup"><span data-stu-id="f0701-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="f0701-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="f0701-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="f0701-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0701-166">**SettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="f0701-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0701-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f0701-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0701-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f0701-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0701-169">O nome da classe derivada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que implementa as configurações para esse tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0701-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0701-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0701-170">Remarks</span></span>

<span data-ttu-id="f0701-171">O acesso à classe **Msvm \_ ResourceTypeDefinition** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="f0701-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f0701-172">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f0701-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0701-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0701-173">Requirements</span></span>



| <span data-ttu-id="f0701-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0701-174">Requirement</span></span> | <span data-ttu-id="f0701-175">Valor</span><span class="sxs-lookup"><span data-stu-id="f0701-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0701-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0701-176">Minimum supported client</span></span><br/> | <span data-ttu-id="f0701-177">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0701-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0701-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0701-178">Minimum supported server</span></span><br/> | <span data-ttu-id="f0701-179">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0701-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0701-180">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f0701-180">End of client support</span></span><br/>    | <span data-ttu-id="f0701-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f0701-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f0701-182">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f0701-182">End of server support</span></span><br/>    | <span data-ttu-id="f0701-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f0701-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f0701-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0701-184">Namespace</span></span><br/>                | <span data-ttu-id="f0701-185">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f0701-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0701-186">MOF</span><span class="sxs-lookup"><span data-stu-id="f0701-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0701-187"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0701-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0701-188">DLL</span><span class="sxs-lookup"><span data-stu-id="f0701-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0701-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0701-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

