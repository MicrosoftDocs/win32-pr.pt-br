---
description: Representa uma unidade de disco físico, como visto por um computador que executa o sistema operacional Windows.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Classe Win32_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501033"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="b0540-103">\_Classe Win32 DiskDrive</span><span class="sxs-lookup"><span data-stu-id="b0540-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="b0540-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDrive do Win32** representa uma unidade de disco físico, como visto por um computador que executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="b0540-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="b0540-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b0540-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b0540-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b0540-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0540-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0540-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="b0540-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b0540-108">Members</span></span>

<span data-ttu-id="b0540-109">A classe **Win32 \_ DiskDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b0540-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b0540-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0540-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0540-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0540-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0540-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0540-112">Methods</span></span>

<span data-ttu-id="b0540-113">A classe **Win32 \_ DiskDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b0540-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="b0540-114">Método</span><span class="sxs-lookup"><span data-stu-id="b0540-114">Method</span></span>            | <span data-ttu-id="b0540-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0540-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0540-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="b0540-116">**Reset**</span></span>         | <span data-ttu-id="b0540-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="b0540-117">Not implemented.</span></span> <span data-ttu-id="b0540-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ DiskDrive**](cim-diskdrive.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="b0540-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b0540-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b0540-119">**SetPowerState**</span></span> | <span data-ttu-id="b0540-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="b0540-120">Not implemented.</span></span> <span data-ttu-id="b0540-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ DiskDrive**](cim-diskdrive.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="b0540-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b0540-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0540-122">Properties</span></span>

<span data-ttu-id="b0540-123">A classe **Win32 \_ DiskDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0540-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0540-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="b0540-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-127">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b0540-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-128">Availability and status of the device.</span></span>

<span data-ttu-id="b0540-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b0540-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b0540-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0540-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b0540-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b0540-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b0540-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="b0540-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b0540-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b0540-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b0540-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="b0540-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b0540-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="b0540-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b0540-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="b0540-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b0540-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="b0540-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b0540-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="b0540-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b0540-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="b0540-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b0540-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="b0540-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b0540-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="b0540-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b0540-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="b0540-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b0540-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b0540-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="b0540-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="b0540-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b0540-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="b0540-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b0540-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="b0540-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b0540-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b0540-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="b0540-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b0540-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b0540-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b0540-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b0540-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b0540-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="b0540-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b0540-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="b0540-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-156">A unidade de disco não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b0540-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-157">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="b0540-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-158">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-160">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api de \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b0540-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-161">Número de bytes em cada setor para a unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="b0540-162">Exemplo: 512</span><span class="sxs-lookup"><span data-stu-id="b0540-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="b0540-163">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="b0540-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-164">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0540-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-166">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="b0540-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-167">Matriz de recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="b0540-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="b0540-168">Por exemplo, o dispositivo pode dar suporte a acesso aleatório (3), mídia removível (7) e limpeza automática (9).</span><span class="sxs-lookup"><span data-stu-id="b0540-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="b0540-169">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0540-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b0540-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b0540-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b0540-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="b0540-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="b0540-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="b0540-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="b0540-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="b0540-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="b0540-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="b0540-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="b0540-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="b0540-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="b0540-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="b0540-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="b0540-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-178">Dá suporte a mídia removível</span><span class="sxs-lookup"><span data-stu-id="b0540-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="b0540-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="b0540-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="b0540-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="b0540-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="b0540-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="b0540-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="b0540-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="b0540-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-183">Dá suporte à mídia Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="b0540-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="b0540-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="b0540-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-185">A ejeção antes da desmontagem da unidade não é necessária</span><span class="sxs-lookup"><span data-stu-id="b0540-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-186">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b0540-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-187">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0540-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-189">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="b0540-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-190">Lista de explicações mais detalhadas para qualquer um dos recursos do dispositivo de acesso indicados na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="b0540-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="b0540-191">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="b0540-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="b0540-192">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-193">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b0540-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-194">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-196">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b0540-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-197">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b0540-197">Short description of the object.</span></span>

<span data-ttu-id="b0540-198">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b0540-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-202">Algoritmo ou ferramenta usada pelo dispositivo para dar suporte à compactação.</span><span class="sxs-lookup"><span data-stu-id="b0540-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="b0540-203">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b0540-204">O nome do algoritmo de compactação ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0540-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="b0540-205">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b0540-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b0540-206">Se o dispositivo dá suporte a recursos de compactação ou não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b0540-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="b0540-207">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="b0540-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b0540-208">O dispositivo dá suporte a recursos de compactação, mas seu esquema de compactação não é conhecido ou não foi divulgado.</span><span class="sxs-lookup"><span data-stu-id="b0540-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="b0540-209">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="b0540-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b0540-210">O dispositivo não oferece suporte à compactação.</span><span class="sxs-lookup"><span data-stu-id="b0540-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b0540-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-212">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-214">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b0540-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-215">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b0540-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b0540-216">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b0540-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="b0540-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b0540-218"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="b0540-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-219">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b0540-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="b0540-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b0540-221">(1)</span><span class="sxs-lookup"><span data-stu-id="b0540-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-222">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b0540-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b0540-224">(2)</span><span class="sxs-lookup"><span data-stu-id="b0540-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b0540-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="b0540-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b0540-226">(3)</span><span class="sxs-lookup"><span data-stu-id="b0540-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-227">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="b0540-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b0540-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="b0540-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b0540-229">(4)</span><span class="sxs-lookup"><span data-stu-id="b0540-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-230">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-230">Device is not working properly.</span></span> <span data-ttu-id="b0540-231">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b0540-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b0540-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="b0540-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b0540-233">(5)</span><span class="sxs-lookup"><span data-stu-id="b0540-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-234">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="b0540-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b0540-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="b0540-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b0540-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="b0540-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-237">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b0540-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b0540-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="b0540-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b0540-239">(7)</span><span class="sxs-lookup"><span data-stu-id="b0540-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b0540-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="b0540-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b0540-241">(8)</span><span class="sxs-lookup"><span data-stu-id="b0540-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-242">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="b0540-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b0540-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="b0540-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b0540-244">(9)</span><span class="sxs-lookup"><span data-stu-id="b0540-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-245">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-245">Device is not working properly.</span></span> <span data-ttu-id="b0540-246">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b0540-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="b0540-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b0540-248">(10)</span><span class="sxs-lookup"><span data-stu-id="b0540-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-249">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b0540-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="b0540-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b0540-251">(11)</span><span class="sxs-lookup"><span data-stu-id="b0540-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-252">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b0540-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="b0540-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b0540-254">12</span><span class="sxs-lookup"><span data-stu-id="b0540-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-255">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="b0540-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b0540-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b0540-257">(13)</span><span class="sxs-lookup"><span data-stu-id="b0540-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-258">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b0540-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="b0540-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b0540-260">(14)</span><span class="sxs-lookup"><span data-stu-id="b0540-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-261">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="b0540-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b0540-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="b0540-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b0540-263">(15)</span><span class="sxs-lookup"><span data-stu-id="b0540-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-264">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="b0540-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b0540-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="b0540-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b0540-266">(16)</span><span class="sxs-lookup"><span data-stu-id="b0540-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-267">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="b0540-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b0540-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="b0540-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b0540-269">(17)</span><span class="sxs-lookup"><span data-stu-id="b0540-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-270">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b0540-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b0540-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b0540-272">(18)</span><span class="sxs-lookup"><span data-stu-id="b0540-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-273">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="b0540-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b0540-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="b0540-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b0540-275">(19)</span><span class="sxs-lookup"><span data-stu-id="b0540-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b0540-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="b0540-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b0540-277">(20)</span><span class="sxs-lookup"><span data-stu-id="b0540-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-278">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b0540-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b0540-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b0540-280">(21)</span><span class="sxs-lookup"><span data-stu-id="b0540-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-281">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="b0540-281">System failure.</span></span> <span data-ttu-id="b0540-282">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="b0540-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b0540-283">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b0540-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="b0540-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b0540-285">(22)</span><span class="sxs-lookup"><span data-stu-id="b0540-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-286">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b0540-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b0540-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="b0540-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b0540-288">(23)</span><span class="sxs-lookup"><span data-stu-id="b0540-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-289">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="b0540-289">System failure.</span></span> <span data-ttu-id="b0540-290">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="b0540-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b0540-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="b0540-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b0540-292">(24)</span><span class="sxs-lookup"><span data-stu-id="b0540-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-293">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="b0540-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b0540-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b0540-295">(25)</span><span class="sxs-lookup"><span data-stu-id="b0540-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-296">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b0540-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b0540-298">(26)</span><span class="sxs-lookup"><span data-stu-id="b0540-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-299">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b0540-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="b0540-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b0540-301">(27)</span><span class="sxs-lookup"><span data-stu-id="b0540-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-302">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="b0540-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b0540-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="b0540-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b0540-304">(28)</span><span class="sxs-lookup"><span data-stu-id="b0540-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-305">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="b0540-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b0540-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="b0540-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b0540-307">(29)</span><span class="sxs-lookup"><span data-stu-id="b0540-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-308">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b0540-308">Device is disabled.</span></span> <span data-ttu-id="b0540-309">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="b0540-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b0540-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="b0540-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b0540-311">(30)</span><span class="sxs-lookup"><span data-stu-id="b0540-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-312">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b0540-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b0540-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b0540-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b0540-314">(31)</span><span class="sxs-lookup"><span data-stu-id="b0540-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-315">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-315">Device is not working properly.</span></span> <span data-ttu-id="b0540-316">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="b0540-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b0540-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-318">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0540-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-320">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b0540-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-321">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b0540-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b0540-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0540-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-326">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b0540-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b0540-327">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b0540-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b0540-328">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b0540-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b0540-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-330">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="b0540-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-331">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-333">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b0540-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-334">Tamanho de bloco padrão, em bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="b0540-335">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b0540-336">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-337">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b0540-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-340">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b0540-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-341">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b0540-341">Description of the object.</span></span>

<span data-ttu-id="b0540-342">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b0540-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-346">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b0540-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-347">Identificador exclusivo da unidade de disco com outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="b0540-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="b0540-348">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b0540-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-350">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0540-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-352">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="b0540-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b0540-353">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b0540-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-357">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="b0540-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="b0540-358">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b0540-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-362">Tipo de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="b0540-363">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-364">**FirmwareRevision**</span><span class="sxs-lookup"><span data-stu-id="b0540-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-367">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ \_ descritor de dispositivo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="b0540-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-368">Revisão do firmware da unidade de disco atribuída pelo fabricante.</span><span class="sxs-lookup"><span data-stu-id="b0540-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b0540-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="b0540-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-370">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-372">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| funções do Windows 95/98 Functions \| \_ Mapear \_ informações \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="b0540-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-373">Número da unidade física da unidade especificada.</span><span class="sxs-lookup"><span data-stu-id="b0540-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="b0540-374">Essa propriedade é preenchida pela estrutura de [**\_ \_ número do dispositivo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) retornada do código de controle [**\_ \_ obter \_ \_ número de dispositivo de armazenamento de IOCTL**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .</span><span class="sxs-lookup"><span data-stu-id="b0540-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="b0540-375">Um valor de 0xFFFFFFFF indica que a unidade especificada não é mapeada para uma unidade física.</span><span class="sxs-lookup"><span data-stu-id="b0540-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="b0540-376">Example: 1</span><span class="sxs-lookup"><span data-stu-id="b0540-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="b0540-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b0540-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-378">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b0540-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-380">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b0540-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-381">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b0540-381">Date and time the object was installed.</span></span> <span data-ttu-id="b0540-382">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b0540-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b0540-383">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="b0540-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-385">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-387">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de entrada e saída de dispositivo do win32api \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="b0540-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-388">Tipo de interface da unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="b0540-389">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="b0540-389">The values are:</span></span>

<span data-ttu-id="b0540-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="b0540-390">SCSI</span></span>

<span data-ttu-id="b0540-391">HDC</span><span class="sxs-lookup"><span data-stu-id="b0540-391">HDC</span></span>

<span data-ttu-id="b0540-392">IDE</span><span class="sxs-lookup"><span data-stu-id="b0540-392">IDE</span></span>

<span data-ttu-id="b0540-393">USB</span><span class="sxs-lookup"><span data-stu-id="b0540-393">USB</span></span>

<span data-ttu-id="b0540-394">1394</span><span class="sxs-lookup"><span data-stu-id="b0540-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="b0540-395">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b0540-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-396">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-398">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0540-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b0540-399">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-400">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="b0540-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-403">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ hardware \\ \\ DEVICEMAP \\ \\ SCSI \\ \\ SCSI porta \\ \\ SCSI Bus ID \\ \\ \\ \\ ID de unidade lógica \\ \\ ", "Win32Registry \| manufacturer")</span><span class="sxs-lookup"><span data-stu-id="b0540-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-404">Nome do fabricante da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="b0540-405">Exemplo: "Seagate"</span><span class="sxs-lookup"><span data-stu-id="b0540-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="b0540-406">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b0540-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-407">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-409">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b0540-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-410">Tamanho máximo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="b0540-411">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b0540-412">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-413">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="b0540-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-414">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-416">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="b0540-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-417">Tamanho máximo de mídia, em quilobytes, de mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="b0540-418">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b0540-419">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-420">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="b0540-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-421">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0540-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-423">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("as \| estruturas de entrada e saída do dispositivo win32api de \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| \| FixedMedia")</span><span class="sxs-lookup"><span data-stu-id="b0540-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-424">Se for **true**, a mídia de uma unidade de disco será carregada, o que significa que o dispositivo tem um sistema de arquivos legível e está acessível.</span><span class="sxs-lookup"><span data-stu-id="b0540-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="b0540-425">Para unidades de disco fixas, essa propriedade será sempre **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="b0540-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="b0540-426">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="b0540-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-429">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo do win32api \| " MediaType de [**disco \_**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="b0540-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-430">Tipo de mídia usada ou acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="b0540-431">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="b0540-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="b0540-432">**Mídia de disco rígido externo**</span><span class="sxs-lookup"><span data-stu-id="b0540-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="b0540-433">**Mídia removível** ("mídia removível diferente de disquete")</span><span class="sxs-lookup"><span data-stu-id="b0540-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="b0540-434">**Disco rígido fixo** ("mídia de disco rígido fixa")</span><span class="sxs-lookup"><span data-stu-id="b0540-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0540-435">**Desconhecido** ("formato desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b0540-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-436">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b0540-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-437">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-439">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b0540-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-440">Tamanho mínimo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="b0540-441">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b0540-442">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-443">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="b0540-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-444">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-446">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ hardware \\ \\ DEVICEMAP \\ \\ SCSI \\ \\ SCSI porta \\ \\ SCSI Bus ID \\ \\ \\ \\ ID de unidade lógica \\ \\ ", "Win32Registry \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="b0540-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-447">O número do modelo do fabricante da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="b0540-448">Exemplo: "ST32171W"</span><span class="sxs-lookup"><span data-stu-id="b0540-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="b0540-449">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b0540-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-450">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-452">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b0540-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-453">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b0540-453">Label by which the object is known.</span></span> <span data-ttu-id="b0540-454">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b0540-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b0540-455">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-456">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="b0540-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-457">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0540-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-459">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="b0540-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="b0540-460">Se a limpeza manual ou automática for possível, ela será indicada na propriedade **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b0540-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="b0540-461">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-462">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="b0540-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-463">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-465">Número máximo de mídias que podem ser suportadas ou inseridas (quando o dispositivo de acesso à mídia dá suporte a várias mídias individuais).</span><span class="sxs-lookup"><span data-stu-id="b0540-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="b0540-466">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-467">**Partições**</span><span class="sxs-lookup"><span data-stu-id="b0540-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-468">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-470">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| informações de partição de estruturas de entrada e saída de dispositivo win32api \| [**\_**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition")</span><span class="sxs-lookup"><span data-stu-id="b0540-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-471">Número de partições nesta unidade de disco físico que são reconhecidas pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0540-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="b0540-472">Exemplo: 2</span><span class="sxs-lookup"><span data-stu-id="b0540-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="b0540-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b0540-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-476">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b0540-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-477">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0540-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b0540-478">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b0540-479">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b0540-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b0540-480">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b0540-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-481">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0540-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-483">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0540-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b0540-484">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="b0540-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0540-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b0540-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b0540-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="b0540-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-487">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b0540-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b0540-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b0540-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b0540-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-490">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b0540-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b0540-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b0540-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-492">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="b0540-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b0540-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="b0540-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-494">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b0540-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b0540-495">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="b0540-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="b0540-496">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b0540-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b0540-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="b0540-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-498">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="b0540-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b0540-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="b0540-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b0540-500">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="b0540-500">Timed Power-On Supported</span></span>

<span data-ttu-id="b0540-501">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="b0540-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b0540-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-503">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0540-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0540-505">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="b0540-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b0540-506">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="b0540-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b0540-507">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="b0540-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-509">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-510">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-511">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo de win32api caminho de \| [**\_ endereço SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| ")</span><span class="sxs-lookup"><span data-stu-id="b0540-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-512">Número de barramento SCSI da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="b0540-513">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="b0540-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="b0540-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="b0540-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-515">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-516">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-517">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api LUN de \| [**\_ endereço SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| ")</span><span class="sxs-lookup"><span data-stu-id="b0540-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-518">LUN (número de unidade lógica) SCSI da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="b0540-519">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="b0540-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="b0540-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="b0540-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-521">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-522">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-523">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída do dispositivo de win32api] \| [**\_ endereço SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PortNumber")</span><span class="sxs-lookup"><span data-stu-id="b0540-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-524">Número da porta SCSI da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="b0540-525">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="b0540-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="b0540-526">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="b0540-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-527">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-528">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-529">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo de win32api de destino de \| [**\_ endereço SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| ")</span><span class="sxs-lookup"><span data-stu-id="b0540-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-530">Número de identificador SCSI da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="b0540-531">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="b0540-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="b0540-532">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="b0540-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-533">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-534">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-535">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")</span><span class="sxs-lookup"><span data-stu-id="b0540-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-536">Número de setores em cada faixa para esta unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="b0540-537">Exemplo: 63</span><span class="sxs-lookup"><span data-stu-id="b0540-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="b0540-538">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b0540-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-539">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-540">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-541">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ \_ descritor de dispositivo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="b0540-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-542">Número alocado pelo fabricante para identificar a mídia física.</span><span class="sxs-lookup"><span data-stu-id="b0540-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="b0540-543">Exemplo: WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="b0540-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="b0540-544">**Signature**</span><span class="sxs-lookup"><span data-stu-id="b0540-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-545">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-546">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-547">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída do dispositivo win32api \| " assinatura de [**\_ \_ informações de layout da unidade**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| ")</span><span class="sxs-lookup"><span data-stu-id="b0540-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-548">Identificação do disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-548">Disk identification.</span></span> <span data-ttu-id="b0540-549">Essa propriedade pode ser usada para identificar um recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b0540-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="b0540-550">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="b0540-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-551">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-552">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-553">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b0540-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-554">Tamanho da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-554">Size of the disk drive.</span></span> <span data-ttu-id="b0540-555">Ele é calculado multiplicando o número total de cilindros, faixas em cada cilindro, setores em cada faixa e bytes em cada setor.</span><span class="sxs-lookup"><span data-stu-id="b0540-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="b0540-556">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-557">**Status**</span><span class="sxs-lookup"><span data-stu-id="b0540-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-558">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-559">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-560">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b0540-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-561">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b0540-561">Current status of the object.</span></span> <span data-ttu-id="b0540-562">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="b0540-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b0540-563">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b0540-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b0540-564">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b0540-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b0540-565">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b0540-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b0540-566">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b0540-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b0540-567">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b0540-568">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="b0540-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b0540-569">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b0540-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b0540-570">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b0540-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b0540-571">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b0540-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0540-572">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b0540-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b0540-573">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b0540-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b0540-574">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b0540-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b0540-575">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b0540-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b0540-576">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b0540-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b0540-577">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b0540-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b0540-578">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b0540-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b0540-579">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b0540-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b0540-580">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b0540-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b0540-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-582">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0540-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-583">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-584">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="b0540-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-585">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b0540-585">State of the logical device.</span></span> <span data-ttu-id="b0540-586">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="b0540-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b0540-587">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b0540-588">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b0540-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0540-589">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b0540-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b0540-590">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b0540-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b0540-591">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="b0540-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b0540-592">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="b0540-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0540-593">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0540-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-594">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-595">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-596">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b0540-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b0540-597">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="b0540-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b0540-598">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-599">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b0540-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-600">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0540-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-601">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-602">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b0540-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b0540-603">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b0540-603">Name of the scoping system.</span></span>

<span data-ttu-id="b0540-604">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="b0540-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-606">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-607">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-608">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| " cilindros de [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="b0540-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-609">Número total de cilindros na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="b0540-610">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b0540-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b0540-611">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="b0540-612">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="b0540-613">Exemplo: 657</span><span class="sxs-lookup"><span data-stu-id="b0540-613">Example: 657</span></span>

<span data-ttu-id="b0540-614">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="b0540-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-616">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-617">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-618">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="b0540-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-619">Número total de cabeçotes na unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="b0540-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="b0540-620">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b0540-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b0540-621">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="b0540-622">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="b0540-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="b0540-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-624">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-625">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-626">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")</span><span class="sxs-lookup"><span data-stu-id="b0540-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-627">Número total de setores na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="b0540-628">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b0540-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b0540-629">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="b0540-630">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="b0540-631">Exemplo: 2649024</span><span class="sxs-lookup"><span data-stu-id="b0540-631">Example: 2649024</span></span>

<span data-ttu-id="b0540-632">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="b0540-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-634">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b0540-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-635">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-636">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="b0540-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-637">Número total de faixas na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="b0540-638">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b0540-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b0540-639">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="b0540-640">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="b0540-641">Exemplo: 42048</span><span class="sxs-lookup"><span data-stu-id="b0540-641">Example: 42048</span></span>

<span data-ttu-id="b0540-642">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b0540-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b0540-643">**TrackPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="b0540-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0540-644">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0540-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0540-645">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0540-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0540-646">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ geometria de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="b0540-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="b0540-647">Número de faixas em cada cilindro na unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="b0540-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="b0540-648">Observação: o valor dessa propriedade é obtido por meio de funções estendidas de interrupção do BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b0540-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b0540-649">O valor poderá ser impreciso se a unidade usar um esquema de tradução para dar suporte a tamanhos de disco de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="b0540-650">Consulte o fabricante para obter especificações precisas da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="b0540-651">Exemplo: 64</span><span class="sxs-lookup"><span data-stu-id="b0540-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0540-652">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0540-652">Remarks</span></span>

<span data-ttu-id="b0540-653">As unidades de disco rígido físico são o meio de armazenamento principal para informações em qualquer ambiente computacional.</span><span class="sxs-lookup"><span data-stu-id="b0540-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="b0540-654">Embora as organizações geralmente usem dispositivos como unidades de fita e unidades de CD para arquivar dados, esses dispositivos não são adequados para o armazenamento diário de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="b0540-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="b0540-655">Somente discos rígidos físicos oferecem a velocidade e a facilidade de uso necessários para armazenar dados e para executar aplicativos e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b0540-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="b0540-656">Para gerenciar dados com eficiência, é importante ter um inventário detalhado de todos os seus discos físicos, seus recursos e suas capacidades.</span><span class="sxs-lookup"><span data-stu-id="b0540-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="b0540-657">Você pode usar a classe **Win32 \_ DiskDrive** para derivar esse tipo de inventário.</span><span class="sxs-lookup"><span data-stu-id="b0540-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="b0540-658">Qualquer interface para uma unidade de disco físico do Windows é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="b0540-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="b0540-659">Os recursos da unidade de disco vistos por esse objeto correspondem às características lógica e de gerenciamento da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="b0540-660">Em alguns casos, isso pode não refletir as características físicas reais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0540-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="b0540-661">Qualquer objeto baseado em outro dispositivo lógico não seria um membro desta classe.</span><span class="sxs-lookup"><span data-stu-id="b0540-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="b0540-662">Por motivos de segurança, um usuário que se conecta a partir de um computador remoto deve ter o privilégio do **sc \_ Manager \_ Connect** habilitado para poder enumerar essa classe.</span><span class="sxs-lookup"><span data-stu-id="b0540-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="b0540-663">Para obter mais informações, consulte [segurança de serviço e direitos de acesso](/windows/desktop/Services/service-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="b0540-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="b0540-664">A classe **Win32 \_ DiskDrive** é derivada de [**\_ DiskDrive CIM**](cim-diskdrive.md) que deriva do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="b0540-665">A classe **CIM \_ MediaAccessDevice** deriva do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b0540-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b0540-666">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b0540-666">Examples</span></span>

<span data-ttu-id="b0540-667">O exemplo de código de [relatório de inventário de servidores-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) do PowerShell na galeria do TechNet usa várias classes, incluindo **Win32 \_ DiskDrive**, para retornar informações sobre o status do servidor.</span><span class="sxs-lookup"><span data-stu-id="b0540-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="b0540-668">A [unidade do mapa para a letra da unidade usando a \_ propriedade tipo de interface do Win32 DiskDrive](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) exemplo de código do PowerShell mapeia uma unidade para uma letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="b0540-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0540-669">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0540-669">Requirements</span></span>



| <span data-ttu-id="b0540-670">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0540-670">Requirement</span></span> | <span data-ttu-id="b0540-671">Valor</span><span class="sxs-lookup"><span data-stu-id="b0540-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0540-672">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0540-672">Minimum supported client</span></span><br/> | <span data-ttu-id="b0540-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0540-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0540-674">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0540-674">Minimum supported server</span></span><br/> | <span data-ttu-id="b0540-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0540-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0540-676">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0540-676">Namespace</span></span><br/>                | <span data-ttu-id="b0540-677">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b0540-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0540-678">MOF</span><span class="sxs-lookup"><span data-stu-id="b0540-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0540-679"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0540-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0540-680">DLL</span><span class="sxs-lookup"><span data-stu-id="b0540-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0540-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0540-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0540-682">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0540-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0540-683">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="b0540-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="b0540-684">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="b0540-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b0540-685">Tarefas do WMI: discos e sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="b0540-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

