---
description: A \_ classe CIM DiskPartition representa um intervalo contíguo de blocos lógicos que é identificável pelo sistema operacional por meio dos campos tipo e subtipo da partição.
ms.assetid: 22a0e5be-c66b-40a2-9a7a-047d2edc0278
ms.tgt_platform: multiple
title: Classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition
- CIM_DiskPartition.Access
- CIM_DiskPartition.Availability
- CIM_DiskPartition.BlockSize
- CIM_DiskPartition.Bootable
- CIM_DiskPartition.Caption
- CIM_DiskPartition.ConfigManagerErrorCode
- CIM_DiskPartition.ConfigManagerUserConfig
- CIM_DiskPartition.CreationClassName
- CIM_DiskPartition.Description
- CIM_DiskPartition.DeviceID
- CIM_DiskPartition.ErrorCleared
- CIM_DiskPartition.ErrorDescription
- CIM_DiskPartition.ErrorMethodology
- CIM_DiskPartition.InstallDate
- CIM_DiskPartition.LastErrorCode
- CIM_DiskPartition.Name
- CIM_DiskPartition.NumberOfBlocks
- CIM_DiskPartition.PNPDeviceID
- CIM_DiskPartition.PowerManagementCapabilities
- CIM_DiskPartition.PowerManagementSupported
- CIM_DiskPartition.PrimaryPartition
- CIM_DiskPartition.Purpose
- CIM_DiskPartition.Status
- CIM_DiskPartition.StatusInfo
- CIM_DiskPartition.SystemCreationClassName
- CIM_DiskPartition.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d1761e140813c26e67594872df5a8d2f7361768b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826528"
---
# <a name="cim_diskpartition-class"></a><span data-ttu-id="c5744-103">\_Classe CIM DiskPartition</span><span class="sxs-lookup"><span data-stu-id="c5744-103">CIM\_DiskPartition class</span></span>

<span data-ttu-id="c5744-104">A classe **CIM \_ DiskPartition** representa um intervalo contíguo de blocos lógicos que é identificável pelo sistema operacional por meio dos campos tipo e subtipo da partição.</span><span class="sxs-lookup"><span data-stu-id="c5744-104">The **CIM\_DiskPartition** class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="c5744-105">As partições de disco devem ser realizadas diretamente pela mídia física (indicada pela Associação de [**\_ RealizesDiskPartition do CIM**](cim-realizesdiskpartition.md) ) ou criados em volumes de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5744-105">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5744-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c5744-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c5744-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c5744-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c5744-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c5744-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c5744-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c5744-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5744-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5744-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C541-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskPartition : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  boolean  Bootable;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="c5744-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c5744-111">Members</span></span>

<span data-ttu-id="c5744-112">A classe **CIM \_ DiskPartition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c5744-112">The **CIM\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="c5744-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5744-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c5744-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5744-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5744-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c5744-115">Methods</span></span>

<span data-ttu-id="c5744-116">A classe **CIM \_ DiskPartition** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c5744-116">The **CIM\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="c5744-117">Método</span><span class="sxs-lookup"><span data-stu-id="c5744-117">Method</span></span>                                                                   | <span data-ttu-id="c5744-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5744-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5744-119">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c5744-119">**Reset**</span></span>](reset-method-in-class-cim-diskpartition.md)                 | <span data-ttu-id="c5744-120">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5744-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="c5744-121">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c5744-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c5744-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c5744-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-diskpartition.md) | <span data-ttu-id="c5744-123">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="c5744-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c5744-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c5744-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c5744-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5744-125">Properties</span></span>

<span data-ttu-id="c5744-126">A classe **CIM \_ DiskPartition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c5744-126">The **CIM\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5744-127">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="c5744-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5744-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-130">Especifica se a mídia é legível, gravável ou ambas, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="c5744-130">Specifies whether the media is readable, writeable, or both, for example.</span></span> <span data-ttu-id="c5744-131">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5744-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c5744-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-133">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c5744-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c5744-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="c5744-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-135">Seres.</span><span class="sxs-lookup"><span data-stu-id="c5744-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c5744-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="c5744-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-137">Gravável.</span><span class="sxs-lookup"><span data-stu-id="c5744-137">Writeable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c5744-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="c5744-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-139">Suporte de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c5744-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c5744-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="c5744-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-141">Gravar uma vez.</span><span class="sxs-lookup"><span data-stu-id="c5744-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c5744-142">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="c5744-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5744-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-145">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c5744-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-146">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-146">Availability and status of the device.</span></span>

<span data-ttu-id="c5744-147">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c5744-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c5744-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5744-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c5744-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c5744-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c5744-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c5744-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="c5744-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c5744-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="c5744-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c5744-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="c5744-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c5744-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="c5744-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c5744-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="c5744-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c5744-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="c5744-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c5744-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c5744-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c5744-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c5744-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c5744-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="c5744-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c5744-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="c5744-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-161">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c5744-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c5744-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="c5744-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-163">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="c5744-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c5744-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c5744-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-165">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c5744-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c5744-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="c5744-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c5744-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="c5744-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-168">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c5744-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c5744-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c5744-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-170">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c5744-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c5744-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="c5744-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-172">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="c5744-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c5744-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c5744-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-174">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="c5744-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c5744-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="c5744-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-176">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="c5744-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c5744-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c5744-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-178">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5744-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-180">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="c5744-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-181">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5744-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="c5744-182">Se for um tamanho de bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c5744-182">If it is a variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="c5744-183">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira o valor 1.</span><span class="sxs-lookup"><span data-stu-id="c5744-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter the value 1.</span></span>

<span data-ttu-id="c5744-184">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c5744-185">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c5744-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-186">**Inicializável**</span><span class="sxs-lookup"><span data-stu-id="c5744-186">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-187">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c5744-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-189">Se **for true**, a partição de disco será rotulada como inicializável.</span><span class="sxs-lookup"><span data-stu-id="c5744-189">If **TRUE**, the disk partition is labeled as bootable.</span></span> <span data-ttu-id="c5744-190">Isso não significa que um sistema operacional seja carregado na partição.</span><span class="sxs-lookup"><span data-stu-id="c5744-190">This does not mean that an operating system is loaded on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="c5744-191">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c5744-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-194">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c5744-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-195">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c5744-195">Short textual description of the object.</span></span>

<span data-ttu-id="c5744-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-197">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c5744-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-198">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5744-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-200">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c5744-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-201">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c5744-201">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="c5744-202">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c5744-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c5744-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c5744-204"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="c5744-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-205">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5744-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c5744-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c5744-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c5744-207">(1)</span><span class="sxs-lookup"><span data-stu-id="c5744-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-208">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5744-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c5744-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c5744-210">(2)</span><span class="sxs-lookup"><span data-stu-id="c5744-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c5744-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c5744-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c5744-212">(3)</span><span class="sxs-lookup"><span data-stu-id="c5744-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-213">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="c5744-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c5744-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c5744-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c5744-215">(4)</span><span class="sxs-lookup"><span data-stu-id="c5744-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-216">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="c5744-216">Device is not working properly.</span></span> <span data-ttu-id="c5744-217">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c5744-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c5744-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="c5744-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c5744-219">(5)</span><span class="sxs-lookup"><span data-stu-id="c5744-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-220">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="c5744-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c5744-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c5744-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c5744-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="c5744-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-223">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c5744-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c5744-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c5744-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c5744-225">(7)</span><span class="sxs-lookup"><span data-stu-id="c5744-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c5744-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="c5744-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c5744-227">(8)</span><span class="sxs-lookup"><span data-stu-id="c5744-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-228">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="c5744-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c5744-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="c5744-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c5744-230">(9)</span><span class="sxs-lookup"><span data-stu-id="c5744-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-231">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-231">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c5744-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="c5744-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c5744-233">(10)</span><span class="sxs-lookup"><span data-stu-id="c5744-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-234">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c5744-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="c5744-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c5744-236">(11)</span><span class="sxs-lookup"><span data-stu-id="c5744-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-237">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c5744-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="c5744-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c5744-239">12</span><span class="sxs-lookup"><span data-stu-id="c5744-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-240">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="c5744-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c5744-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c5744-242">(13)</span><span class="sxs-lookup"><span data-stu-id="c5744-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-243">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c5744-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="c5744-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c5744-245">(14)</span><span class="sxs-lookup"><span data-stu-id="c5744-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-246">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="c5744-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c5744-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="c5744-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c5744-248">(15)</span><span class="sxs-lookup"><span data-stu-id="c5744-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-249">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="c5744-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c5744-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="c5744-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c5744-251">(16)</span><span class="sxs-lookup"><span data-stu-id="c5744-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-252">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="c5744-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c5744-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="c5744-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c5744-254">(17)</span><span class="sxs-lookup"><span data-stu-id="c5744-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-255">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c5744-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c5744-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c5744-257">(18)</span><span class="sxs-lookup"><span data-stu-id="c5744-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-258">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="c5744-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c5744-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="c5744-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c5744-260">(19)</span><span class="sxs-lookup"><span data-stu-id="c5744-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c5744-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c5744-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c5744-262">(20)</span><span class="sxs-lookup"><span data-stu-id="c5744-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-263">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="c5744-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c5744-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c5744-265">(21)</span><span class="sxs-lookup"><span data-stu-id="c5744-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-266">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c5744-266">System failure.</span></span> <span data-ttu-id="c5744-267">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c5744-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c5744-268">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c5744-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c5744-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c5744-270">(22)</span><span class="sxs-lookup"><span data-stu-id="c5744-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-271">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c5744-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c5744-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="c5744-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c5744-273">(23)</span><span class="sxs-lookup"><span data-stu-id="c5744-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-274">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="c5744-274">System failure.</span></span> <span data-ttu-id="c5744-275">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="c5744-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c5744-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="c5744-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c5744-277">(24)</span><span class="sxs-lookup"><span data-stu-id="c5744-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-278">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="c5744-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c5744-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c5744-280">(25)</span><span class="sxs-lookup"><span data-stu-id="c5744-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-281">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c5744-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c5744-283">(26)</span><span class="sxs-lookup"><span data-stu-id="c5744-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-284">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5744-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c5744-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="c5744-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c5744-286">(27)</span><span class="sxs-lookup"><span data-stu-id="c5744-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-287">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="c5744-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c5744-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="c5744-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c5744-289">(28)</span><span class="sxs-lookup"><span data-stu-id="c5744-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-290">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="c5744-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c5744-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="c5744-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c5744-292">(29)</span><span class="sxs-lookup"><span data-stu-id="c5744-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-293">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="c5744-293">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c5744-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c5744-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c5744-295">(30)</span><span class="sxs-lookup"><span data-stu-id="c5744-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-296">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="c5744-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c5744-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c5744-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c5744-298">(31)</span><span class="sxs-lookup"><span data-stu-id="c5744-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-299">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="c5744-299">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c5744-300">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c5744-300">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-301">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c5744-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-303">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c5744-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-304">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c5744-304">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c5744-305">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-306">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c5744-306">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-309">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5744-309">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5744-310">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c5744-310">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c5744-311">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c5744-311">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c5744-312">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-313">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c5744-313">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-316">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c5744-316">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-317">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c5744-317">Textual description of the object.</span></span>

<span data-ttu-id="c5744-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-319">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c5744-319">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-322">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5744-322">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5744-323">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5744-323">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c5744-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c5744-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-326">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c5744-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-328">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="c5744-328">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c5744-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c5744-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-331">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-333">Cadeia de caracteres de forma livre que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="c5744-333">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c5744-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-335">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c5744-335">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-338">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5744-338">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="c5744-339">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-339">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-340">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c5744-340">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-341">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c5744-341">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-343">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c5744-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-344">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c5744-344">Date and time the object was installed.</span></span> <span data-ttu-id="c5744-345">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c5744-345">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c5744-346">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c5744-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-348">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5744-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-350">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5744-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c5744-351">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-352">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c5744-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-355">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c5744-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-356">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c5744-356">Label by which the object is known.</span></span> <span data-ttu-id="c5744-357">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c5744-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c5744-358">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-359">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c5744-359">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-360">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5744-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-362">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="c5744-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-363">Número de blocos consecutivos, cada um deles bloqueia o tamanho do valor contido na propriedade **BlockSize** , que forma a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5744-363">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="c5744-364">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c5744-364">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="c5744-365">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c5744-365">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="c5744-366">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-366">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c5744-367">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c5744-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-368">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c5744-368">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-371">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c5744-371">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-372">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5744-372">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="c5744-373">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c5744-374">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c5744-374">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c5744-375">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c5744-375">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-376">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5744-376">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c5744-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-378">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5744-378">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c5744-379">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="c5744-379">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5744-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c5744-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c5744-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="c5744-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c5744-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c5744-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c5744-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c5744-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-384">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c5744-384">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c5744-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c5744-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-386">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="c5744-386">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c5744-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="c5744-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-388">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c5744-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c5744-389">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="c5744-389">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c5744-390">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c5744-390">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c5744-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="c5744-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-392">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="c5744-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c5744-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="c5744-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c5744-394">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="c5744-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c5744-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c5744-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-396">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c5744-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-398">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c5744-398">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c5744-399">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c5744-399">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c5744-400">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="c5744-400">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c5744-401">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c5744-401">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="c5744-402">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-403">**Partição Primária**</span><span class="sxs-lookup"><span data-stu-id="c5744-403">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-404">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c5744-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-406">Se for **true**, a partição de disco será rotulada como a partição primária para um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="c5744-406">If **TRUE**, the disk partition is labeled as the primary partition for a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c5744-407">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="c5744-407">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-408">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5744-410">Descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="c5744-410">Describes the media and its use.</span></span>

<span data-ttu-id="c5744-411">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-411">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-412">**Status**</span><span class="sxs-lookup"><span data-stu-id="c5744-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-413">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-415">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c5744-415">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-416">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c5744-416">Current status of the object.</span></span>

<span data-ttu-id="c5744-417">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-417">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c5744-418">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c5744-418">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c5744-419">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c5744-419">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c5744-420">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c5744-420">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c5744-421">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c5744-421">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5744-422">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c5744-422">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c5744-423">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c5744-423">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c5744-424">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c5744-424">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c5744-425">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c5744-425">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c5744-426">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c5744-426">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c5744-427">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c5744-427">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c5744-428">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c5744-428">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c5744-429">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c5744-429">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c5744-430">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c5744-430">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5744-431">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c5744-431">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-432">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c5744-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-434">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="c5744-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c5744-435">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c5744-435">State of the logical device.</span></span> <span data-ttu-id="c5744-436">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c5744-436">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c5744-437">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c5744-438">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c5744-438">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c5744-439">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c5744-439">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c5744-440">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c5744-440">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c5744-441">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c5744-441">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c5744-442">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="c5744-442">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c5744-443">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c5744-443">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-444">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-446">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5744-446">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5744-447">Propriedade **CreationClassName** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c5744-447">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="c5744-448">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5744-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c5744-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5744-450">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c5744-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5744-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5744-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5744-452">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c5744-452">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c5744-453">Propriedade de **nome** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c5744-453">Scoping system's **Name** property.</span></span>

<span data-ttu-id="c5744-454">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5744-455">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5744-455">Remarks</span></span>

<span data-ttu-id="c5744-456">A classe **CIM \_ DiskPartition** é derivada de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-456">The **CIM\_DiskPartition** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c5744-457">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c5744-457">WMI does not implement this class.</span></span> <span data-ttu-id="c5744-458">Para classes derivadas do **CIM \_ DiskPartition**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c5744-458">For classes derived from **CIM\_DiskPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c5744-459">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c5744-459">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c5744-460">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c5744-460">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5744-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5744-461">Requirements</span></span>



| <span data-ttu-id="c5744-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5744-462">Requirement</span></span> | <span data-ttu-id="c5744-463">Valor</span><span class="sxs-lookup"><span data-stu-id="c5744-463">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5744-464">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5744-464">Minimum supported client</span></span><br/> | <span data-ttu-id="c5744-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5744-465">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5744-466">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5744-466">Minimum supported server</span></span><br/> | <span data-ttu-id="c5744-467">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5744-467">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5744-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5744-468">Namespace</span></span><br/>                | <span data-ttu-id="c5744-469">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c5744-469">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5744-470">MOF</span><span class="sxs-lookup"><span data-stu-id="c5744-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5744-471"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5744-471"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5744-472">DLL</span><span class="sxs-lookup"><span data-stu-id="c5744-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5744-473"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5744-473"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5744-474">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5744-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5744-475">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="c5744-475">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

