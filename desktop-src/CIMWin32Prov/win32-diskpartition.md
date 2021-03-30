---
description: Representa os recursos e a capacidade de gerenciamento de uma área particionada de um disco físico em um sistema de computador executando o Windows.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Classe Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826584"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="94380-103">\_Classe Win32 DiskPartition</span><span class="sxs-lookup"><span data-stu-id="94380-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="94380-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskPartition do Win32** representa os recursos e a capacidade de gerenciamento de uma área particionada de um disco físico em um sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="94380-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="94380-105">Exemplo: disco \# 0, partição \# 1.</span><span class="sxs-lookup"><span data-stu-id="94380-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="94380-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="94380-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="94380-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="94380-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94380-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94380-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="94380-109">Membros</span><span class="sxs-lookup"><span data-stu-id="94380-109">Members</span></span>

<span data-ttu-id="94380-110">A classe **Win32 \_ DiskPartition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94380-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="94380-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="94380-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="94380-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94380-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94380-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="94380-113">Methods</span></span>

<span data-ttu-id="94380-114">A classe **Win32 \_ DiskPartition** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="94380-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="94380-115">Método</span><span class="sxs-lookup"><span data-stu-id="94380-115">Method</span></span>                                                     | <span data-ttu-id="94380-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="94380-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94380-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="94380-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="94380-118">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94380-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="94380-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="94380-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="94380-120">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="94380-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="94380-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94380-121">Properties</span></span>

<span data-ttu-id="94380-122">A classe **Win32 \_ DiskPartition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="94380-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94380-123">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="94380-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-124">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94380-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94380-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-126">Acesso à mídia disponível.</span><span class="sxs-lookup"><span data-stu-id="94380-126">Media access available.</span></span>

<span data-ttu-id="94380-127">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94380-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="94380-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="94380-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="94380-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="94380-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="94380-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="94380-131">Gravável</span><span class="sxs-lookup"><span data-stu-id="94380-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="94380-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="94380-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="94380-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="94380-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="94380-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-135">Tipo de dados: **unit16**</span><span class="sxs-lookup"><span data-stu-id="94380-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="94380-136">Tipo de acesso: somente gravação</span><span class="sxs-lookup"><span data-stu-id="94380-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-137">Disponibilidade e status adicionais do dispositivo, além do especificado na propriedade de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="94380-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="94380-138">A propriedade de **disponibilidade** denota o status primário e a disponibilidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94380-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="94380-139">Em alguns casos, isso não será suficiente para indicar o status completo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94380-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="94380-140">Nesses casos, a propriedade **AdditionalAvailability** pode ser usada para fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="94380-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="94380-141">Por exemplo, a **disponibilidade** primária de um dispositivo pode estar off-line (valor = 8), mas também pode estar em um estado de baixa energia (valor **AdditonalAvailability** = 14), ou o dispositivo pode estar executando o diagnóstico (**AdditionalAvailability** valor = 5, em teste). "</span><span class="sxs-lookup"><span data-stu-id="94380-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="94380-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94380-143">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="94380-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-144">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="94380-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="94380-145">**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="94380-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="94380-146">**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="94380-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="94380-147">**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="94380-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="94380-148">**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="94380-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="94380-149">**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="94380-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="94380-150">**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="94380-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="94380-151">**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="94380-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="94380-152">**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="94380-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="94380-153">**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="94380-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="94380-154">**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="94380-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="94380-155">Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="94380-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="94380-156">Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="94380-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="94380-157">**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="94380-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="94380-158">**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="94380-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="94380-159">Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="94380-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="94380-160">Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="94380-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="94380-161">**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="94380-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="94380-162">**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="94380-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="94380-163">**Desativar** (21)</span><span class="sxs-lookup"><span data-stu-id="94380-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-164">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="94380-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-165">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94380-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94380-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-167">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="94380-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="94380-168">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94380-168">Availability and status of the device.</span></span>

<span data-ttu-id="94380-169">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94380-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="94380-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="94380-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="94380-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="94380-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="94380-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="94380-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="94380-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="94380-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="94380-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="94380-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="94380-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="94380-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="94380-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="94380-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="94380-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="94380-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="94380-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="94380-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="94380-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="94380-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="94380-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="94380-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="94380-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="94380-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="94380-183">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="94380-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="94380-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="94380-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="94380-185">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="94380-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="94380-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="94380-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="94380-187">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="94380-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="94380-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="94380-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="94380-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="94380-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="94380-190">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="94380-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="94380-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="94380-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="94380-192">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="94380-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="94380-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="94380-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="94380-194">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="94380-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="94380-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="94380-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="94380-196">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="94380-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="94380-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="94380-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="94380-198">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="94380-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="94380-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-200">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-202">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="94380-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="94380-203">Tamanho em bytes dos blocos que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94380-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="94380-204">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1.</span><span class="sxs-lookup"><span data-stu-id="94380-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="94380-205">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94380-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="94380-206">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94380-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-207">**Inicializável**</span><span class="sxs-lookup"><span data-stu-id="94380-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-208">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-210">Indica se o computador pode ser inicializado a partir dessa partição.</span><span class="sxs-lookup"><span data-stu-id="94380-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="94380-211">Essa propriedade é herdada do [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="94380-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-212">**BootPartition**</span><span class="sxs-lookup"><span data-stu-id="94380-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-213">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-215">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="94380-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="94380-216">Partição é a partição ativa.</span><span class="sxs-lookup"><span data-stu-id="94380-216">Partition is the active partition.</span></span> <span data-ttu-id="94380-217">O sistema operacional usa a partição ativa ao inicializar a partir de um disco rígido.</span><span class="sxs-lookup"><span data-stu-id="94380-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="94380-218">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="94380-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-219">Tipo de dados: **cadeia de caracteres.**</span><span class="sxs-lookup"><span data-stu-id="94380-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="94380-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-221">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="94380-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="94380-222">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="94380-222">Short description of the object.</span></span>

<span data-ttu-id="94380-223">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94380-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="94380-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-225">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94380-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94380-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-227">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="94380-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="94380-228">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="94380-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="94380-229">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="94380-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="94380-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="94380-231"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="94380-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="94380-232">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="94380-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="94380-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="94380-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="94380-234">(1)</span><span class="sxs-lookup"><span data-stu-id="94380-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="94380-235">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="94380-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="94380-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="94380-237">(2)</span><span class="sxs-lookup"><span data-stu-id="94380-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="94380-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="94380-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="94380-239">(3)</span><span class="sxs-lookup"><span data-stu-id="94380-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="94380-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="94380-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="94380-241">(4)</span><span class="sxs-lookup"><span data-stu-id="94380-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="94380-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="94380-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="94380-243">(5)</span><span class="sxs-lookup"><span data-stu-id="94380-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="94380-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="94380-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="94380-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="94380-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="94380-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="94380-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="94380-247">(7)</span><span class="sxs-lookup"><span data-stu-id="94380-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="94380-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="94380-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="94380-249">(8)</span><span class="sxs-lookup"><span data-stu-id="94380-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="94380-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="94380-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="94380-251">(9)</span><span class="sxs-lookup"><span data-stu-id="94380-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="94380-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="94380-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="94380-253">(10)</span><span class="sxs-lookup"><span data-stu-id="94380-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="94380-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="94380-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="94380-255">(11)</span><span class="sxs-lookup"><span data-stu-id="94380-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="94380-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="94380-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="94380-257">12</span><span class="sxs-lookup"><span data-stu-id="94380-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="94380-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="94380-259">(13)</span><span class="sxs-lookup"><span data-stu-id="94380-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="94380-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="94380-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="94380-261">(14)</span><span class="sxs-lookup"><span data-stu-id="94380-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="94380-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="94380-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="94380-263">(15)</span><span class="sxs-lookup"><span data-stu-id="94380-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="94380-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="94380-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="94380-265">(16)</span><span class="sxs-lookup"><span data-stu-id="94380-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="94380-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="94380-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="94380-267">(17)</span><span class="sxs-lookup"><span data-stu-id="94380-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="94380-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="94380-269">(18)</span><span class="sxs-lookup"><span data-stu-id="94380-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="94380-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="94380-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="94380-271">(19)</span><span class="sxs-lookup"><span data-stu-id="94380-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="94380-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="94380-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="94380-273">(20)</span><span class="sxs-lookup"><span data-stu-id="94380-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="94380-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="94380-275">(21)</span><span class="sxs-lookup"><span data-stu-id="94380-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="94380-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="94380-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="94380-277">(22)</span><span class="sxs-lookup"><span data-stu-id="94380-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="94380-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="94380-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="94380-279">(23)</span><span class="sxs-lookup"><span data-stu-id="94380-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="94380-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="94380-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="94380-281">(24)</span><span class="sxs-lookup"><span data-stu-id="94380-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="94380-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="94380-283">(25)</span><span class="sxs-lookup"><span data-stu-id="94380-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="94380-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="94380-285">(26)</span><span class="sxs-lookup"><span data-stu-id="94380-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="94380-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="94380-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="94380-287">(27)</span><span class="sxs-lookup"><span data-stu-id="94380-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="94380-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="94380-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="94380-289">(28)</span><span class="sxs-lookup"><span data-stu-id="94380-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="94380-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="94380-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="94380-291">(29)</span><span class="sxs-lookup"><span data-stu-id="94380-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="94380-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="94380-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="94380-293">(30)</span><span class="sxs-lookup"><span data-stu-id="94380-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="94380-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="94380-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="94380-295">(31)</span><span class="sxs-lookup"><span data-stu-id="94380-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="94380-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-297">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-299">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="94380-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="94380-300">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="94380-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="94380-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="94380-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-303">Tipo de dados: **cadeia de caracteres.**</span><span class="sxs-lookup"><span data-stu-id="94380-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="94380-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-305">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="94380-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="94380-306">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="94380-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="94380-307">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="94380-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="94380-308">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-309">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="94380-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-312">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="94380-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="94380-313">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="94380-313">Description of the object.</span></span>

<span data-ttu-id="94380-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94380-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="94380-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-318">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="94380-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="94380-319">Identificador exclusivo da unidade de disco e da partição, do restante do sistema.</span><span class="sxs-lookup"><span data-stu-id="94380-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="94380-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="94380-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-321">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94380-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94380-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-323">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="94380-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="94380-324">Número de índice do disco que contém esta partição.</span><span class="sxs-lookup"><span data-stu-id="94380-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="94380-325">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="94380-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="94380-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="94380-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-327">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-329">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="94380-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="94380-330">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="94380-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-334">Informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="94380-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="94380-335">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-336">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="94380-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-337">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-339">Tipo de detecção de erro e correção com suporte nesta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94380-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="94380-340">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94380-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-341">**HiddenSectors**</span><span class="sxs-lookup"><span data-stu-id="94380-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-342">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94380-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94380-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-344">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api")</span><span class="sxs-lookup"><span data-stu-id="94380-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="94380-345">Número de setores ocultos na partição.</span><span class="sxs-lookup"><span data-stu-id="94380-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="94380-346">Exemplo: 63</span><span class="sxs-lookup"><span data-stu-id="94380-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="94380-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="94380-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-348">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="94380-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-350">Uma matriz de cadeias de caracteres de forma livre que fornece explicações e detalhes por trás das entradas na matriz OtherIdentifyingInfo.</span><span class="sxs-lookup"><span data-stu-id="94380-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="94380-351">Observe que cada entrada dessa matriz está relacionada à entrada em OtherIdentifyingInfo que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="94380-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="94380-352">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="94380-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-354">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94380-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94380-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-356">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="94380-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="94380-357">Número de índice da partição.</span><span class="sxs-lookup"><span data-stu-id="94380-357">Index number of the partition.</span></span>

<span data-ttu-id="94380-358">Example: 1</span><span class="sxs-lookup"><span data-stu-id="94380-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="94380-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="94380-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-360">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="94380-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94380-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-362">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="94380-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="94380-363">Data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="94380-363">Date the object was installed.</span></span> <span data-ttu-id="94380-364">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="94380-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="94380-365">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94380-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-366">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="94380-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-367">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94380-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94380-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-369">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94380-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="94380-370">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-371">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="94380-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-372">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-374">Qualificadores: **preterida**</span><span class="sxs-lookup"><span data-stu-id="94380-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="94380-375">Tempo máximo em milissegundos, que um dispositivo pode executar em um estado desativado.</span><span class="sxs-lookup"><span data-stu-id="94380-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="94380-376">O estado de um dispositivo é definido em suas propriedades de disponibilidade e AdditionalAvailability, onde desativado é transmitido pelo valor 21.</span><span class="sxs-lookup"><span data-stu-id="94380-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="94380-377">O que ocorre ao final do limite de tempo é específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94380-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="94380-378">O dispositivo pode unquiesce, pode estar offline ou executar outra ação.</span><span class="sxs-lookup"><span data-stu-id="94380-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="94380-379">Um valor de 0 indica que um dispositivo pode permanecer desativado indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="94380-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="94380-380">"A propriedade MaxQuiesceTime foi preterida.</span><span class="sxs-lookup"><span data-stu-id="94380-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="94380-381">Ao avaliar o uso de desativar, ele estava determinando que essa única propriedade não é adequada para descrever quando um dispositivo sairá automaticamente de um estado inativo.</span><span class="sxs-lookup"><span data-stu-id="94380-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="94380-382">Na verdade, o cenário mais provável para um dispositivo sair de um estado inativo foi determinado com base no número de solicitações pendentes enfileiradas em vez de em um tempo máximo.</span><span class="sxs-lookup"><span data-stu-id="94380-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="94380-383">Isso será avaliado novamente e reposicionado mais tarde.</span><span class="sxs-lookup"><span data-stu-id="94380-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="94380-384">\\n</span><span class="sxs-lookup"><span data-stu-id="94380-384">\\n</span></span>

 

<span data-ttu-id="94380-385">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-386">**Nome**</span><span class="sxs-lookup"><span data-stu-id="94380-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-389">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="94380-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="94380-390">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="94380-390">Label by which the object is known.</span></span> <span data-ttu-id="94380-391">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="94380-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="94380-392">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94380-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="94380-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-394">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-396">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="94380-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="94380-397">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94380-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="94380-398">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="94380-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="94380-399">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94380-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="94380-400">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94380-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="94380-401">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94380-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="94380-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-403">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-405">Matriz que captura dados adicionais, além das informações de DeviceID, que podem ser usadas para identificar um LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="94380-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="94380-406">Um exemplo seria manter o nome amigável do usuário do sistema operacional para o dispositivo nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="94380-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="94380-407">O comprimento máximo é 256.</span><span class="sxs-lookup"><span data-stu-id="94380-407">Maximum length is 256.</span></span>

<span data-ttu-id="94380-408">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="94380-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-410">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-412">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="94380-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="94380-413">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94380-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="94380-414">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="94380-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="94380-415">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-416">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="94380-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-417">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94380-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="94380-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-419">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94380-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="94380-420">Os valores de matriz, 0 = "desconhecido", 1 = "sem suporte" e 2 = "desabilitado" são auto-explicativos.</span><span class="sxs-lookup"><span data-stu-id="94380-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="94380-421">O valor 3 = "Enabled" indica que os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="94380-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="94380-422">"Modos de economia de energia inseridos automaticamente" (4) descreve que um dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="94380-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="94380-423">"Estado de energia configurável" (5) indica que há suporte para o método SetPowerState.</span><span class="sxs-lookup"><span data-stu-id="94380-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="94380-424">"Ciclo de energia com suporte" (6) indica que o método SetPowerState pode ser invocado com a variável de entrada PowerState definida como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="94380-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="94380-425">"Energia cronometrada com suporte" (7) indica que o método SetPowerState pode ser invocado com a variável de entrada PowerState definida como 5 ("ciclo de energia") e o parâmetro de tempo definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="94380-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="94380-426">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-427">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="94380-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="94380-428">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="94380-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="94380-429">**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="94380-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="94380-430">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="94380-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="94380-431">**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="94380-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="94380-432">**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="94380-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="94380-433">**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="94380-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="94380-434">**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="94380-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="94380-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-436">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-438">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="94380-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="94380-439">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="94380-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="94380-440">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-441">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="94380-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-442">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-444">O número de horas consecutivas em que este dispositivo foi ligado, desde seu último ciclo de energia.</span><span class="sxs-lookup"><span data-stu-id="94380-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="94380-445">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-446">**Partição Primária**</span><span class="sxs-lookup"><span data-stu-id="94380-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-447">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-449">Se for **true**, esta é a partição primária.</span><span class="sxs-lookup"><span data-stu-id="94380-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="94380-450">Essa propriedade é herdada do [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="94380-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-451">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="94380-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-452">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-454">Descrição da mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="94380-454">Description of the media and its use.</span></span>

<span data-ttu-id="94380-455">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="94380-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-456">**RewritePartition**</span><span class="sxs-lookup"><span data-stu-id="94380-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-457">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94380-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94380-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-459">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| informações de partição de estruturas de entrada e saída de dispositivo win32api \| [**\_**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RewritePartition")</span><span class="sxs-lookup"><span data-stu-id="94380-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="94380-460">Se **for true**, as informações de partição foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="94380-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="94380-461">Quando você altera uma partição (com [**o \_ \_ layout de \_ unidade \_ do conjunto de discos do IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), o sistema usa essa propriedade para determinar quais partições foram alteradas e precisam de suas informações regravadas.</span><span class="sxs-lookup"><span data-stu-id="94380-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="94380-462">Se **for true**, a partição deverá ser reescrita.</span><span class="sxs-lookup"><span data-stu-id="94380-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="94380-463">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="94380-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-464">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-466">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| ReadFile"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="94380-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="94380-467">Tamanho total da partição.</span><span class="sxs-lookup"><span data-stu-id="94380-467">Total size of the partition.</span></span>

<span data-ttu-id="94380-468">Exemplo: 1059045376</span><span class="sxs-lookup"><span data-stu-id="94380-468">Example: 1059045376</span></span>

<span data-ttu-id="94380-469">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94380-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="94380-470">**StartingOffset**</span><span class="sxs-lookup"><span data-stu-id="94380-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-471">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-473">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| ReadFile"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="94380-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="94380-474">Deslocamento inicial (em bytes) da partição.</span><span class="sxs-lookup"><span data-stu-id="94380-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="94380-475">Exemplo: 32256</span><span class="sxs-lookup"><span data-stu-id="94380-475">Example: 32256</span></span>

<span data-ttu-id="94380-476">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94380-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="94380-477">**Status**</span><span class="sxs-lookup"><span data-stu-id="94380-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-478">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-479">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-480">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="94380-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="94380-481">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="94380-481">Current status of the object.</span></span> <span data-ttu-id="94380-482">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="94380-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="94380-483">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="94380-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="94380-484">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="94380-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="94380-485">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="94380-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="94380-486">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="94380-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="94380-487">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="94380-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="94380-488">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="94380-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="94380-489">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="94380-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="94380-490">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="94380-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="94380-491">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="94380-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-492">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="94380-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="94380-493">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="94380-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="94380-494">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="94380-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="94380-495">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="94380-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="94380-496">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="94380-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="94380-497">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="94380-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="94380-498">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="94380-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="94380-499">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="94380-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="94380-500">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="94380-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="94380-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-502">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94380-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94380-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-504">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="94380-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="94380-505">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="94380-505">State of the logical device.</span></span> <span data-ttu-id="94380-506">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="94380-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="94380-507">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="94380-508">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="94380-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-509">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="94380-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="94380-510">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="94380-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="94380-511">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="94380-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="94380-512">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="94380-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94380-513">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="94380-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-514">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-515">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-516">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="94380-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="94380-517">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="94380-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="94380-518">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-519">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="94380-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-521">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-522">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="94380-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="94380-523">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="94380-523">Name of the scoping system.</span></span>

<span data-ttu-id="94380-524">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-525">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="94380-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-526">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94380-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94380-527">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94380-528">O número total de horas em que este dispositivo foi ligado.</span><span class="sxs-lookup"><span data-stu-id="94380-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="94380-529">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="94380-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="94380-530">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="94380-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94380-531">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="94380-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="94380-532">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94380-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94380-533">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| PartitionRecord \| dwPartitionType")</span><span class="sxs-lookup"><span data-stu-id="94380-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="94380-534">Tipo da partição.</span><span class="sxs-lookup"><span data-stu-id="94380-534">Type of the partition.</span></span>

<span data-ttu-id="94380-535">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="94380-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="94380-536">Não utilizado</span><span class="sxs-lookup"><span data-stu-id="94380-536">"Unused"</span></span></dd> <dd><span data-ttu-id="94380-537">"FAT de 12 bits"</span><span class="sxs-lookup"><span data-stu-id="94380-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="94380-538">"Xenix tipo 1"</span><span class="sxs-lookup"><span data-stu-id="94380-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="94380-539">"Xenix tipo 2"</span><span class="sxs-lookup"><span data-stu-id="94380-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="94380-540">"FAT de 16 bits"</span><span class="sxs-lookup"><span data-stu-id="94380-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="94380-541">"Partição estendida"</span><span class="sxs-lookup"><span data-stu-id="94380-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="94380-542">"MS-DOS v4 enorme"</span><span class="sxs-lookup"><span data-stu-id="94380-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="94380-543">"Sistema de arquivos instalável"</span><span class="sxs-lookup"><span data-stu-id="94380-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="94380-544">"Plataforma de referência de PowerPC"</span><span class="sxs-lookup"><span data-stu-id="94380-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="94380-545">UNIX</span><span class="sxs-lookup"><span data-stu-id="94380-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="94380-546">NT</span><span class="sxs-lookup"><span data-stu-id="94380-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="94380-547">"Win95 w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="94380-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="94380-548">"Estendido c/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="94380-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="94380-549">"Gerenciador de discos lógicos"</span><span class="sxs-lookup"><span data-stu-id="94380-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="94380-550">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="94380-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="94380-551">**Não utilizado** ("não utilizado")</span><span class="sxs-lookup"><span data-stu-id="94380-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="94380-552">**Fat de 12 bits** ("Fat de 12 bits")</span><span class="sxs-lookup"><span data-stu-id="94380-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="94380-553">**Xenix tipo 1** ("Xenix tipo 1")</span><span class="sxs-lookup"><span data-stu-id="94380-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="94380-554">**Xenix tipo 2** ("Xenix tipo 2")</span><span class="sxs-lookup"><span data-stu-id="94380-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="94380-555">**Fat de 16 bits** ("Fat de 16 bits")</span><span class="sxs-lookup"><span data-stu-id="94380-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="94380-556">**Partição estendida** ("partição estendida")</span><span class="sxs-lookup"><span data-stu-id="94380-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="94380-557">**MS-dos v4 enorme** ("MS-dos v4 enorme")</span><span class="sxs-lookup"><span data-stu-id="94380-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="94380-558">**Sistema de arquivos instalável** ("sistema de arquivos instalável")</span><span class="sxs-lookup"><span data-stu-id="94380-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="94380-559">**Plataforma de referência PowerPC** (plataforma de referência PowerPC)</span><span class="sxs-lookup"><span data-stu-id="94380-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="94380-560">**Unix** ("Unix")</span><span class="sxs-lookup"><span data-stu-id="94380-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="94380-561">**NTFS** ("NTFS")</span><span class="sxs-lookup"><span data-stu-id="94380-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="94380-562">**Win95 w/Extended int 13** ("Win95 w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="94380-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="94380-563">**Estendido c/Extended int 13** ("Extended w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="94380-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="94380-564">**Gerenciador de discos lógicos** ("Gerenciador de discos lógicos")</span><span class="sxs-lookup"><span data-stu-id="94380-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94380-565">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="94380-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="94380-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="94380-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="94380-567">Comentários</span><span class="sxs-lookup"><span data-stu-id="94380-567">Remarks</span></span>

<span data-ttu-id="94380-568">A classe **Win32 \_ DiskPartition** é derivada de [**CIM \_ DiskPartition**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="94380-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="94380-569">Uma partição é uma divisão estrutural de uma unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="94380-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="94380-570">Embora uma unidade possa conter uma única partição, os volumes maiores geralmente são divididos em várias partições.</span><span class="sxs-lookup"><span data-stu-id="94380-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="94380-571">É por isso que você pode ter as unidades C, D e e, embora seu computador tenha apenas um único disco rígido físico.</span><span class="sxs-lookup"><span data-stu-id="94380-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="94380-572">O Windows dá suporte aos seguintes tipos de partição:</span><span class="sxs-lookup"><span data-stu-id="94380-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="94380-573">Partição primária.</span><span class="sxs-lookup"><span data-stu-id="94380-573">Primary partition.</span></span> <span data-ttu-id="94380-574">Esse é o único tipo de partição que pode ter um sistema operacional instalado.</span><span class="sxs-lookup"><span data-stu-id="94380-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="94380-575">Cada unidade pode ter até quatro partições primárias, cada uma atribuída a uma letra de unidade diferente.</span><span class="sxs-lookup"><span data-stu-id="94380-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="94380-576">Partição estendida.</span><span class="sxs-lookup"><span data-stu-id="94380-576">Extended partition.</span></span> <span data-ttu-id="94380-577">Uma partição adicional que pode ser subdividida em várias unidades lógicas, cada uma atribuída a uma letra de unidade exclusiva.</span><span class="sxs-lookup"><span data-stu-id="94380-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="94380-578">Uma unidade pode ter apenas uma partição estendida; no entanto, você pode dividir essa partição em várias unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="94380-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="94380-579">Isso permite que um disco tenha mais do que apenas as quatro partições primárias permitidas.</span><span class="sxs-lookup"><span data-stu-id="94380-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="94380-580">Partição do sistema.</span><span class="sxs-lookup"><span data-stu-id="94380-580">System partition.</span></span> <span data-ttu-id="94380-581">Qualquer partição primária que contenha um sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="94380-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="94380-582">As partições podem informar como uma unidade de disco físico está realmente sendo usada.</span><span class="sxs-lookup"><span data-stu-id="94380-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="94380-583">Ao examinar as partições físicas em um disco, você pode determinar os seguintes tipos de coisas:</span><span class="sxs-lookup"><span data-stu-id="94380-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="94380-584">Como o disco foi dividido em unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="94380-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="94380-585">Se houver espaço não particionado disponível no disco.</span><span class="sxs-lookup"><span data-stu-id="94380-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="94380-586">Isso pode ser determinado com a subtração do tamanho de todas as partições em um disco do tamanho do disco em si.</span><span class="sxs-lookup"><span data-stu-id="94380-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="94380-587">Se você puder inicializar o computador a partir desse disco (ou seja, o disco conterá uma partição de inicialização).</span><span class="sxs-lookup"><span data-stu-id="94380-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="94380-588">Todas essas perguntas podem ser resolvidas usando a classe **Win32 \_ DiskPartition** .</span><span class="sxs-lookup"><span data-stu-id="94380-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="94380-589">Exemplos</span><span class="sxs-lookup"><span data-stu-id="94380-589">Examples</span></span>

<span data-ttu-id="94380-590">O exemplo de código do PowerShell a seguir verifica o alinhamento dos discos em um computador: se o deslocamento for fracionário, o disco não estará alinhado corretamente.</span><span class="sxs-lookup"><span data-stu-id="94380-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="94380-591">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94380-591">Requirements</span></span>



| <span data-ttu-id="94380-592">Requisito</span><span class="sxs-lookup"><span data-stu-id="94380-592">Requirement</span></span> | <span data-ttu-id="94380-593">Valor</span><span class="sxs-lookup"><span data-stu-id="94380-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94380-594">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94380-594">Minimum supported client</span></span><br/> | <span data-ttu-id="94380-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94380-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94380-596">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94380-596">Minimum supported server</span></span><br/> | <span data-ttu-id="94380-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94380-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94380-598">Namespace</span><span class="sxs-lookup"><span data-stu-id="94380-598">Namespace</span></span><br/>                | <span data-ttu-id="94380-599">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="94380-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94380-600">MOF</span><span class="sxs-lookup"><span data-stu-id="94380-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94380-601"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94380-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94380-602">DLL</span><span class="sxs-lookup"><span data-stu-id="94380-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94380-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94380-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94380-604">Confira também</span><span class="sxs-lookup"><span data-stu-id="94380-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94380-605">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="94380-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="94380-606">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="94380-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="94380-607">Tarefas do WMI: discos e sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="94380-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

