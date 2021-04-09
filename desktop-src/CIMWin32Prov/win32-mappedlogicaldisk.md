---
description: O Win32 \_ MappedLogicalDisk &\# 32; A classe WMI representa os dispositivos de armazenamento em rede que são mapeados como discos lógicos no sistema de computador.
ms.assetid: 5dd4b0eb-7872-4f2d-9c8b-ea03f7e2c16d
ms.tgt_platform: multiple
title: Classe Win32_MappedLogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MappedLogicalDisk
- Win32_MappedLogicalDisk.Reset
- Win32_MappedLogicalDisk.SetPowerState
- Win32_MappedLogicalDisk.Access
- Win32_MappedLogicalDisk.Availability
- Win32_MappedLogicalDisk.BlockSize
- Win32_MappedLogicalDisk.Caption
- Win32_MappedLogicalDisk.Compressed
- Win32_MappedLogicalDisk.ConfigManagerErrorCode
- Win32_MappedLogicalDisk.ConfigManagerUserConfig
- Win32_MappedLogicalDisk.CreationClassName
- Win32_MappedLogicalDisk.Description
- Win32_MappedLogicalDisk.DeviceID
- Win32_MappedLogicalDisk.ErrorCleared
- Win32_MappedLogicalDisk.ErrorDescription
- Win32_MappedLogicalDisk.ErrorMethodology
- Win32_MappedLogicalDisk.FileSystem
- Win32_MappedLogicalDisk.FreeSpace
- Win32_MappedLogicalDisk.InstallDate
- Win32_MappedLogicalDisk.LastErrorCode
- Win32_MappedLogicalDisk.MaximumComponentLength
- Win32_MappedLogicalDisk.Name
- Win32_MappedLogicalDisk.NumberOfBlocks
- Win32_MappedLogicalDisk.PNPDeviceID
- Win32_MappedLogicalDisk.PowerManagementCapabilities
- Win32_MappedLogicalDisk.PowerManagementSupported
- Win32_MappedLogicalDisk.ProviderName
- Win32_MappedLogicalDisk.Purpose
- Win32_MappedLogicalDisk.QuotasDisabled
- Win32_MappedLogicalDisk.QuotasIncomplete
- Win32_MappedLogicalDisk.QuotasRebuilding
- Win32_MappedLogicalDisk.SessionID
- Win32_MappedLogicalDisk.Size
- Win32_MappedLogicalDisk.Status
- Win32_MappedLogicalDisk.StatusInfo
- Win32_MappedLogicalDisk.SupportsDiskQuotas
- Win32_MappedLogicalDisk.SupportsFileBasedCompression
- Win32_MappedLogicalDisk.SystemCreationClassName
- Win32_MappedLogicalDisk.SystemName
- Win32_MappedLogicalDisk.VolumeName
- Win32_MappedLogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c3dfee876c34f36fd0b4cf0b59d3a61afcd75c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089598"
---
# <a name="win32_mappedlogicaldisk-class"></a><span data-ttu-id="34eac-103">\_Classe Win32 MappedLogicalDisk</span><span class="sxs-lookup"><span data-stu-id="34eac-103">Win32\_MappedLogicalDisk class</span></span>

<span data-ttu-id="34eac-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MappedLogicalDisk do Win32** representa os dispositivos de armazenamento em rede que são mapeados como discos lógicos no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="34eac-104">The **Win32\_MappedLogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents network storage devices that are mapped as logical disks on the computer system.</span></span>

<span data-ttu-id="34eac-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="34eac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="34eac-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="34eac-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34eac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34eac-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{BCF02FFE-5560-4de2-B419-272918693426}"), AMENDMENT]
class Win32_MappedLogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   SessionID;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="34eac-108">Membros</span><span class="sxs-lookup"><span data-stu-id="34eac-108">Members</span></span>

<span data-ttu-id="34eac-109">A classe **Win32 \_ MappedLogicalDisk** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="34eac-109">The **Win32\_MappedLogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="34eac-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="34eac-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="34eac-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34eac-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="34eac-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="34eac-112">Methods</span></span>

<span data-ttu-id="34eac-113">A classe **Win32 \_ MappedLogicalDisk** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="34eac-113">The **Win32\_MappedLogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="34eac-114">Método</span><span class="sxs-lookup"><span data-stu-id="34eac-114">Method</span></span>            | <span data-ttu-id="34eac-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="34eac-115">Description</span></span>                                                                                                                                                                                |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34eac-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="34eac-116">**Reset**</span></span>         | <span data-ttu-id="34eac-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="34eac-117">Not implemented.</span></span> <span data-ttu-id="34eac-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>                 |
| <span data-ttu-id="34eac-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="34eac-119">**SetPowerState**</span></span> | <span data-ttu-id="34eac-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="34eac-120">Not implemented.</span></span> <span data-ttu-id="34eac-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="34eac-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34eac-122">Properties</span></span>

<span data-ttu-id="34eac-123">A classe **Win32 \_ MappedLogicalDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="34eac-123">The **Win32\_MappedLogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34eac-124">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="34eac-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34eac-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-127">Estado de acesso do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-127">Device access state.</span></span>

<span data-ttu-id="34eac-128">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34eac-129">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="34eac-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="34eac-130">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="34eac-130">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="34eac-131">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="34eac-131">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="34eac-132">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="34eac-132">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="34eac-133">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="34eac-133">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34eac-134">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="34eac-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34eac-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="34eac-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-138">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-138">Availability and status of the device.</span></span>

<span data-ttu-id="34eac-139">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34eac-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34eac-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34eac-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="34eac-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="34eac-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="34eac-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-143">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="34eac-143">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="34eac-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="34eac-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="34eac-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="34eac-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="34eac-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="34eac-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="34eac-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="34eac-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="34eac-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="34eac-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-149">Offline</span><span class="sxs-lookup"><span data-stu-id="34eac-149">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="34eac-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="34eac-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="34eac-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="34eac-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="34eac-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="34eac-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="34eac-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="34eac-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="34eac-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="34eac-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-155">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="34eac-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="34eac-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="34eac-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-157">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="34eac-157">The device is in a power save state but still functioning and can exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="34eac-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="34eac-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-159">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-159">The device is not functioning, but can be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="34eac-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="34eac-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="34eac-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="34eac-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-162">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="34eac-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="34eac-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="34eac-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-164">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="34eac-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="34eac-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="34eac-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-166">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="34eac-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="34eac-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="34eac-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-168">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="34eac-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="34eac-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="34eac-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-170">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="34eac-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34eac-171">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="34eac-171">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-172">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34eac-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-174">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="34eac-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-175">Tamanho, em bytes, dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="34eac-175">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="34eac-176">Se esse conceito não for válido para o tipo de dispositivo, o valor será 1.</span><span class="sxs-lookup"><span data-stu-id="34eac-176">If this concept is not valid for the device type, the value is 1.</span></span>

<span data-ttu-id="34eac-177">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-177">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="34eac-178">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34eac-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-179">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="34eac-179">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-182">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="34eac-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-183">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="34eac-183">Short description of the object.</span></span>

<span data-ttu-id="34eac-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-185">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="34eac-185">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-186">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-188">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| File System Functions GetVolumeInformation o Vol. de sistema de arquivos \| [](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| \_ \_ é \_ compactado")</span><span class="sxs-lookup"><span data-stu-id="34eac-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-189">Se **for true**, o arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="34eac-189">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="34eac-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-191">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34eac-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-193">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="34eac-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-194">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="34eac-194">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="34eac-195">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="34eac-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="34eac-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="34eac-197"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="34eac-197">(0)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-198">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-198">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="34eac-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="34eac-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="34eac-200">(1)</span><span class="sxs-lookup"><span data-stu-id="34eac-200">(1)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-201">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-201">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="34eac-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="34eac-203">(2)</span><span class="sxs-lookup"><span data-stu-id="34eac-203">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="34eac-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="34eac-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="34eac-205">(3)</span><span class="sxs-lookup"><span data-stu-id="34eac-205">(3)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-206">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="34eac-206">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="34eac-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="34eac-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="34eac-208">(4)</span><span class="sxs-lookup"><span data-stu-id="34eac-208">(4)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-209">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-209">Device is not working properly.</span></span> <span data-ttu-id="34eac-210">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="34eac-210">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="34eac-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="34eac-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="34eac-212">(5)</span><span class="sxs-lookup"><span data-stu-id="34eac-212">(5)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-213">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="34eac-213">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="34eac-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="34eac-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="34eac-215"> (6)</span><span class="sxs-lookup"><span data-stu-id="34eac-215">(6)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-216">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="34eac-216">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="34eac-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="34eac-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="34eac-218">(7)</span><span class="sxs-lookup"><span data-stu-id="34eac-218">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="34eac-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="34eac-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="34eac-220">(8)</span><span class="sxs-lookup"><span data-stu-id="34eac-220">(8)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-221">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="34eac-221">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="34eac-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="34eac-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="34eac-223">(9)</span><span class="sxs-lookup"><span data-stu-id="34eac-223">(9)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-224">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-224">Device is not working properly.</span></span> <span data-ttu-id="34eac-225">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-225">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="34eac-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="34eac-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="34eac-227">(10)</span><span class="sxs-lookup"><span data-stu-id="34eac-227">(10)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-228">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-228">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="34eac-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="34eac-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="34eac-230">(11)</span><span class="sxs-lookup"><span data-stu-id="34eac-230">(11)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-231">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-231">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="34eac-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="34eac-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="34eac-233">12</span><span class="sxs-lookup"><span data-stu-id="34eac-233">(12)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-234">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="34eac-234">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="34eac-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="34eac-236">(13)</span><span class="sxs-lookup"><span data-stu-id="34eac-236">(13)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-237">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-237">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="34eac-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="34eac-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="34eac-239">(14)</span><span class="sxs-lookup"><span data-stu-id="34eac-239">(14)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-240">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="34eac-240">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="34eac-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="34eac-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="34eac-242">(15)</span><span class="sxs-lookup"><span data-stu-id="34eac-242">(15)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-243">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="34eac-243">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="34eac-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="34eac-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="34eac-245">(16)</span><span class="sxs-lookup"><span data-stu-id="34eac-245">(16)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-246">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="34eac-246">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="34eac-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="34eac-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="34eac-248">(17)</span><span class="sxs-lookup"><span data-stu-id="34eac-248">(17)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-249">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="34eac-249">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="34eac-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="34eac-251">(18)</span><span class="sxs-lookup"><span data-stu-id="34eac-251">(18)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-252">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="34eac-252">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="34eac-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="34eac-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="34eac-254">(19)</span><span class="sxs-lookup"><span data-stu-id="34eac-254">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="34eac-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="34eac-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="34eac-256">(20)</span><span class="sxs-lookup"><span data-stu-id="34eac-256">(20)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-257">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="34eac-257">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="34eac-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="34eac-259">(21)</span><span class="sxs-lookup"><span data-stu-id="34eac-259">(21)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-260">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="34eac-260">System failure.</span></span> <span data-ttu-id="34eac-261">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="34eac-261">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="34eac-262">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-262">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="34eac-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="34eac-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="34eac-264">(22)</span><span class="sxs-lookup"><span data-stu-id="34eac-264">(22)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-265">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="34eac-265">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="34eac-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="34eac-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="34eac-267">(23)</span><span class="sxs-lookup"><span data-stu-id="34eac-267">(23)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-268">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="34eac-268">System failure.</span></span> <span data-ttu-id="34eac-269">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="34eac-269">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="34eac-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="34eac-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="34eac-271">(24)</span><span class="sxs-lookup"><span data-stu-id="34eac-271">(24)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-272">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="34eac-272">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="34eac-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="34eac-274">(25)</span><span class="sxs-lookup"><span data-stu-id="34eac-274">(25)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-275">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="34eac-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="34eac-277">(26)</span><span class="sxs-lookup"><span data-stu-id="34eac-277">(26)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-278">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34eac-278">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="34eac-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="34eac-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="34eac-280">(27)</span><span class="sxs-lookup"><span data-stu-id="34eac-280">(27)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-281">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="34eac-281">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="34eac-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="34eac-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="34eac-283">(28)</span><span class="sxs-lookup"><span data-stu-id="34eac-283">(28)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-284">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="34eac-284">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="34eac-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="34eac-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="34eac-286">(29)</span><span class="sxs-lookup"><span data-stu-id="34eac-286">(29)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-287">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="34eac-287">Device is disabled.</span></span> <span data-ttu-id="34eac-288">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="34eac-288">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="34eac-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="34eac-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="34eac-290">(30)</span><span class="sxs-lookup"><span data-stu-id="34eac-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-291">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="34eac-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="34eac-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="34eac-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="34eac-293">(31)</span><span class="sxs-lookup"><span data-stu-id="34eac-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-294">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-294">Device is not working properly.</span></span> <span data-ttu-id="34eac-295">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="34eac-295">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34eac-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="34eac-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-297">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-299">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="34eac-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-300">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="34eac-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="34eac-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34eac-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-305">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34eac-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34eac-306">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="34eac-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="34eac-307">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="34eac-307">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="34eac-308">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-309">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="34eac-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-312">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="34eac-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-313">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="34eac-313">Description of the object.</span></span>

<span data-ttu-id="34eac-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="34eac-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-318">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="34eac-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-319">Identificador exclusivo da matriz de memória.</span><span class="sxs-lookup"><span data-stu-id="34eac-319">Unique identifier of the memory array.</span></span>

<span data-ttu-id="34eac-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="34eac-321">Exemplo: "matriz de memória 1"</span><span class="sxs-lookup"><span data-stu-id="34eac-321">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="34eac-322">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="34eac-322">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-323">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-325">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="34eac-325">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="34eac-326">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-327">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="34eac-327">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-330">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="34eac-330">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span>

<span data-ttu-id="34eac-331">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-332">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="34eac-332">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-335">Tipos de verificação de erros usados pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="34eac-335">Types of error checking used by the hardware.</span></span>

<span data-ttu-id="34eac-336">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-336">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-337">**WPD**</span><span class="sxs-lookup"><span data-stu-id="34eac-337">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-340">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="34eac-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="34eac-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-341">Access type: Read-only</span></span>

<span data-ttu-id="34eac-342">Sistema de arquivos no disco lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-342">File system on the logical disk.</span></span>

<span data-ttu-id="34eac-343">Exemplo: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="34eac-343">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="34eac-344">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="34eac-344">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-345">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34eac-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-347">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="34eac-347">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-348">Espaço disponível no disco lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-348">Space available on the logical disk.</span></span>

<span data-ttu-id="34eac-349">Essa propriedade é herdada [**do \_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-349">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="34eac-350">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34eac-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-351">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="34eac-351">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-352">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="34eac-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-354">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="34eac-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-355">Access type: Read-only</span></span>

<span data-ttu-id="34eac-356">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="34eac-356">Date and time the object was installed.</span></span> <span data-ttu-id="34eac-357">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="34eac-357">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="34eac-358">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-359">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="34eac-359">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-360">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34eac-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-362">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-362">Last error code reported by the logical device.</span></span>

<span data-ttu-id="34eac-363">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-364">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="34eac-364">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-365">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34eac-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-367">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="34eac-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="34eac-368">Contém o comprimento máximo de um componente de nome de arquivo suportado pela unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="34eac-368">Contains the maximum length of a file-name component supported by the Windows drive.</span></span>

<span data-ttu-id="34eac-369">Exemplo: 255</span><span class="sxs-lookup"><span data-stu-id="34eac-369">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="34eac-370">**Nome**</span><span class="sxs-lookup"><span data-stu-id="34eac-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-371">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-373">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="34eac-373">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-374">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="34eac-374">Object label.</span></span>

<span data-ttu-id="34eac-375">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-376">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="34eac-376">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-377">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34eac-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-379">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="34eac-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-380">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="34eac-380">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="34eac-381">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="34eac-381">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="34eac-382">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="34eac-382">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="34eac-383">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-383">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="34eac-384">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34eac-384">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-385">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="34eac-385">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-386">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-388">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="34eac-388">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-389">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-389">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="34eac-390">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="34eac-391">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="34eac-391">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="34eac-392">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="34eac-392">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-393">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34eac-393">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34eac-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-395">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-395">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="34eac-396">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="34eac-396">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34eac-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="34eac-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="34eac-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="34eac-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="34eac-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="34eac-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="34eac-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="34eac-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-401">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="34eac-401">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="34eac-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="34eac-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-403">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="34eac-403">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="34eac-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="34eac-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-405">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="34eac-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="34eac-406">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="34eac-406">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="34eac-407">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="34eac-407">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="34eac-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="34eac-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-409">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="34eac-409">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="34eac-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="34eac-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="34eac-411">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="34eac-411">Timed Power-On Supported</span></span>

<span data-ttu-id="34eac-412">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="34eac-412">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34eac-413">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="34eac-413">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-414">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-414">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-416">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="34eac-416">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="34eac-417">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="34eac-417">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="34eac-418">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-419">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="34eac-419">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-422">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| WNetGetConnection funções de rede do Windows \| ")</span><span class="sxs-lookup"><span data-stu-id="34eac-422">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-423">Nome do caminho de rede para o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-423">Network path name to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-424">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="34eac-424">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-425">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-427">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="34eac-427">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="34eac-428">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-429">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="34eac-429">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-430">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-430">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-432">Se **for true**, o gerenciamento de cotas não estará habilitado para este volume.</span><span class="sxs-lookup"><span data-stu-id="34eac-432">If **True**, quota management is not enabled for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-433">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="34eac-433">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-434">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-434">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-436">Se **for true**, o gerenciamento de cota foi usado, mas foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="34eac-436">If **True**, quota management was used but has been disabled.</span></span> <span data-ttu-id="34eac-437">Incompleto refere-se às informações deixadas no sistema de arquivos após o gerenciamento de cota ter sido desabilitado.</span><span class="sxs-lookup"><span data-stu-id="34eac-437">Incomplete refers to the information left in the file system after quota management has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-438">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="34eac-438">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-439">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-441">Se for **true**, o sistema de arquivos estará configurando para gerenciamento de cotas.</span><span class="sxs-lookup"><span data-stu-id="34eac-441">If **True**, the file system is setting up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-442">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="34eac-442">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-445">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="34eac-445">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="34eac-446">ID da sessão do usuário.</span><span class="sxs-lookup"><span data-stu-id="34eac-446">ID of the user's session.</span></span> <span data-ttu-id="34eac-447">O usuário pode estar conectado usando um logon local ou uma sessão de terminal.</span><span class="sxs-lookup"><span data-stu-id="34eac-447">The user may be connected using a local login or a terminal session.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-448">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="34eac-448">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-449">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="34eac-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-451">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="34eac-451">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-452">Tamanho do disco lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-452">Size of the logical disk.</span></span>

<span data-ttu-id="34eac-453">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="34eac-453">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="34eac-454">Essa propriedade é herdada [**do \_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-454">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-455">**Status**</span><span class="sxs-lookup"><span data-stu-id="34eac-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-456">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-458">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="34eac-458">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-459">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="34eac-459">Current status of the object.</span></span> <span data-ttu-id="34eac-460">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="34eac-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="34eac-461">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitada para inteligente, pode funcionar corretamente, mas prevê uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="34eac-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="34eac-462">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="34eac-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="34eac-463">O status do serviço se aplica ao trabalho administrativo, como espelhamento de espelho de um disco, recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="34eac-463">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="34eac-464">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="34eac-464">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="34eac-465">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="34eac-466">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="34eac-466">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="34eac-467">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="34eac-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="34eac-468">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="34eac-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="34eac-469">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="34eac-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34eac-470">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="34eac-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="34eac-471">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="34eac-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="34eac-472">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="34eac-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="34eac-473">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="34eac-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="34eac-474">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="34eac-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="34eac-475">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="34eac-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="34eac-476">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="34eac-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="34eac-477">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="34eac-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="34eac-478">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="34eac-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34eac-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="34eac-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-480">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34eac-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-482">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="34eac-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-483">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-483">State of the logical device.</span></span> <span data-ttu-id="34eac-484">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="34eac-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="34eac-485">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="34eac-486">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="34eac-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="34eac-487">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="34eac-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="34eac-488">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="34eac-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="34eac-489">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="34eac-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="34eac-490">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="34eac-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="34eac-491">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="34eac-491">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-492">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-492">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34eac-494">Se **for true**, o sistema de arquivos no qual essa unidade de rede está mapeada dá suporte a cotas de disco.</span><span class="sxs-lookup"><span data-stu-id="34eac-494">If **True**, then the file system on which this network drive is mapped supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-495">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="34eac-495">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-496">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="34eac-496">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-498">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ \_ Compact File Compression")</span><span class="sxs-lookup"><span data-stu-id="34eac-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="34eac-499">Se for **true**, a partição de disco lógico dará suporte à compactação baseada em arquivo, como é o caso com NTFS.</span><span class="sxs-lookup"><span data-stu-id="34eac-499">If **True**, the logical disk partition supports file-based compression, such as is the case with NTFS.</span></span> <span data-ttu-id="34eac-500">Essa propriedade é **false** quando a propriedade **compactada** é **true**.</span><span class="sxs-lookup"><span data-stu-id="34eac-500">This property is **False**, when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-501">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="34eac-501">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-502">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-503">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-504">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34eac-504">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34eac-505">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="34eac-505">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="34eac-506">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-506">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-507">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="34eac-507">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-508">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-510">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="34eac-510">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="34eac-511">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="34eac-511">Name of the scoping system.</span></span>

<span data-ttu-id="34eac-512">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-512">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="34eac-513">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="34eac-513">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-514">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-515">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="34eac-515">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="34eac-516">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="34eac-516">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="34eac-517">Nome do volume do disco lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-517">Volume name of the logical disk.</span></span> <span data-ttu-id="34eac-518">Esse valor de propriedade pode ter um máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="34eac-518">This property value can have a maximum of 32 characters.</span></span>

</dd> <dt>

<span data-ttu-id="34eac-519">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="34eac-519">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34eac-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="34eac-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34eac-521">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34eac-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34eac-522">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="34eac-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="34eac-523">Número de série de volume do disco lógico.</span><span class="sxs-lookup"><span data-stu-id="34eac-523">Volume serial number of the logical disk.</span></span> <span data-ttu-id="34eac-524">Esse valor de propriedade pode ter um máximo de 11 caracteres.</span><span class="sxs-lookup"><span data-stu-id="34eac-524">This property value can have a maximum of 11 characters.</span></span>

<span data-ttu-id="34eac-525">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="34eac-525">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="34eac-526">Exemplo: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="34eac-526">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34eac-527">Comentários</span><span class="sxs-lookup"><span data-stu-id="34eac-527">Remarks</span></span>

<span data-ttu-id="34eac-528">As instâncias retornadas para essa classe são as seguintes, suponhamos que o usuário A está enumerando as instâncias:</span><span class="sxs-lookup"><span data-stu-id="34eac-528">The instances returned for this class are as follows, supposing that user A is enumerating the instances:</span></span>

-   <span data-ttu-id="34eac-529">O provedor procura uma sessão de logon do usuário A nesse computador:</span><span class="sxs-lookup"><span data-stu-id="34eac-529">The provider looks for a logon session of user A on that machine:</span></span>

    -   <span data-ttu-id="34eac-530">Se houver uma (e apenas uma) tal sessão de logon, o provedor retornará as unidades mapeadas dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="34eac-530">If there is one (and only one) such logon session, then the provider returns the mapped drives of that session.</span></span>
    -   <span data-ttu-id="34eac-531">Se houver mais de uma sessão para o usuário A no computador, nenhuma instância de unidade mapeada será retornada (porque o provedor não tem uma maneira razoável de decidir qual sessão usar).</span><span class="sxs-lookup"><span data-stu-id="34eac-531">If there is more than one session for user A on the machine, then no mapped drive instances are returned (because the provider has no reasonable way of deciding which session to use).</span></span>

-   <span data-ttu-id="34eac-532">Se não houver sessões do usuário A em execução, e houver um usuário conectado localmente B:</span><span class="sxs-lookup"><span data-stu-id="34eac-532">If there are no sessions of user A running, and there is a locally logged on user B:</span></span>

    -   <span data-ttu-id="34eac-533">Se houver uma única sessão para o usuário B, o provedor representará um e retornará as unidades mapeadas do usuário B. Esse caso dá suporte ao cenário de assistência técnica que deseja ver as instâncias de um usuário conectado localmente.</span><span class="sxs-lookup"><span data-stu-id="34eac-533">If there is a single session for user B, then the provider impersonates A and returns the mapped drives of user B. This case supports the scenario of Helpdesk wanting to see the instances of a locally logged on user.</span></span> <span data-ttu-id="34eac-534">No entanto, se as instâncias são retornadas depende das configurações de política de segurança local nas ferramentas administrativas do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="34eac-534">However, whether instances are returned depends on the Local Security Policy settings in the Control Panel Administrative Tools.</span></span> <span data-ttu-id="34eac-535">Se a política a seguir estiver definida como "Object Creator", nenhuma instância de unidade mapeada será retornada, mesmo que um seja um membro do grupo Administradores:</span><span class="sxs-lookup"><span data-stu-id="34eac-535">If the following policy is set to "Object Creator", then no mapped drive instances are returned, even if A is a member of the Administrators group:</span></span>

        <span data-ttu-id="34eac-536">"Objeto do sistema: proprietário padrão para objetos criados por membros do grupo de administradores".</span><span class="sxs-lookup"><span data-stu-id="34eac-536">"System object: default owner for objects created by members of the administrators group."</span></span>

    -   <span data-ttu-id="34eac-537">Novamente, se houver mais de uma sessão do usuário B em execução no computador, o provedor não terá como decidir qual delas usar.</span><span class="sxs-lookup"><span data-stu-id="34eac-537">Again, if there is more than one session of user B running on the machine, then the provider has no way of deciding which to use.</span></span> <span data-ttu-id="34eac-538">Nesse caso, nenhuma instância de unidade mapeada é retornada.</span><span class="sxs-lookup"><span data-stu-id="34eac-538">In this case, no mapped drive instances are returned.</span></span>

<span data-ttu-id="34eac-539">Para obter mais informações sobre como usar o **Win32 \_ MappedLogicalDisk**, consulte [como posso determinar quais unidades estão mapeadas para compartilhamentos de rede?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span><span class="sxs-lookup"><span data-stu-id="34eac-539">For more information on using **Win32\_MappedLogicalDisk**, see [How Can I Determine Which Drives are Mapped to Network Shares?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="34eac-540">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34eac-540">Examples</span></span>

<span data-ttu-id="34eac-541">O trecho do PowerShell a seguir mostra unidades mapeadas.</span><span class="sxs-lookup"><span data-stu-id="34eac-541">The following PowerShell snippet shows mapped drives.</span></span>


```PowerShell
Get-WmiObject Win32_MappedLogicalDisk | Select Name, ProviderName, FileSystem, Size, FreeSpace | Format-Table
```



## <a name="requirements"></a><span data-ttu-id="34eac-542">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34eac-542">Requirements</span></span>



| <span data-ttu-id="34eac-543">Requisito</span><span class="sxs-lookup"><span data-stu-id="34eac-543">Requirement</span></span> | <span data-ttu-id="34eac-544">Valor</span><span class="sxs-lookup"><span data-stu-id="34eac-544">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34eac-545">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34eac-545">Minimum supported client</span></span><br/> | <span data-ttu-id="34eac-546">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34eac-546">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34eac-547">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34eac-547">Minimum supported server</span></span><br/> | <span data-ttu-id="34eac-548">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34eac-548">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34eac-549">Namespace</span><span class="sxs-lookup"><span data-stu-id="34eac-549">Namespace</span></span><br/>                | <span data-ttu-id="34eac-550">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="34eac-550">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34eac-551">MOF</span><span class="sxs-lookup"><span data-stu-id="34eac-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34eac-552"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34eac-552"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34eac-553">DLL</span><span class="sxs-lookup"><span data-stu-id="34eac-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34eac-554"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34eac-554"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34eac-555">Confira também</span><span class="sxs-lookup"><span data-stu-id="34eac-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34eac-556">**\_LOGICALDISK CIM**</span><span class="sxs-lookup"><span data-stu-id="34eac-556">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="34eac-557">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="34eac-557">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="34eac-558">Tarefas do WMI: discos e sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="34eac-558">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

