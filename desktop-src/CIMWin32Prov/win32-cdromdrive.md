---
description: Representa uma unidade de CD-ROM em um sistema de computador que executa o Windows.
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Classe Win32_CDROMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920502"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="3df06-103">\_Classe Win32 CDROMDrive</span><span class="sxs-lookup"><span data-stu-id="3df06-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="3df06-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CDROMDrive do Win32** representa uma unidade de CD-ROM em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="3df06-105">Lembre-se de que o nome da unidade não corresponde à letra da unidade lógica atribuída ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="3df06-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3df06-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3df06-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3df06-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df06-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3df06-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
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
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="3df06-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3df06-109">Members</span></span>

<span data-ttu-id="3df06-110">A classe **Win32 \_ CDROMDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3df06-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="3df06-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3df06-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3df06-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3df06-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3df06-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3df06-113">Methods</span></span>

<span data-ttu-id="3df06-114">A classe **Win32 \_ CDROMDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3df06-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="3df06-115">Método</span><span class="sxs-lookup"><span data-stu-id="3df06-115">Method</span></span>            | <span data-ttu-id="3df06-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3df06-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df06-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="3df06-117">**Reset**</span></span>         | <span data-ttu-id="3df06-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="3df06-118">Not implemented.</span></span> <span data-ttu-id="3df06-119">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ CDROMDrive**](cim-cdromdrive.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="3df06-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="3df06-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3df06-120">**SetPowerState**</span></span> | <span data-ttu-id="3df06-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="3df06-121">Not implemented.</span></span> <span data-ttu-id="3df06-122">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ CDROMDrive**](cim-cdromdrive.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="3df06-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3df06-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3df06-123">Properties</span></span>

<span data-ttu-id="3df06-124">A classe **Win32 \_ CDROMDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3df06-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3df06-125">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="3df06-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="3df06-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-129">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-129">Availability and status of the device.</span></span>

<span data-ttu-id="3df06-130">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3df06-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3df06-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3df06-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3df06-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3df06-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="3df06-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-134">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="3df06-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3df06-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="3df06-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3df06-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="3df06-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3df06-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="3df06-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3df06-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="3df06-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3df06-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="3df06-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3df06-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="3df06-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3df06-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="3df06-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3df06-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="3df06-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3df06-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="3df06-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3df06-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="3df06-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3df06-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3df06-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="3df06-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="3df06-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3df06-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="3df06-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3df06-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="3df06-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3df06-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="3df06-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="3df06-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3df06-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="3df06-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="3df06-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3df06-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="3df06-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="3df06-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3df06-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="3df06-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="3df06-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3df06-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="3df06-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="3df06-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-161">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="3df06-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-162">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3df06-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-164">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="3df06-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-165">Matriz de recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="3df06-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="3df06-166">Por exemplo, o dispositivo pode dar suporte a acesso aleatório (3), mídia removível (7) e limpeza automática (9).</span><span class="sxs-lookup"><span data-stu-id="3df06-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="3df06-167">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3df06-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3df06-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3df06-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3df06-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="3df06-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="3df06-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="3df06-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="3df06-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="3df06-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="3df06-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="3df06-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="3df06-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="3df06-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="3df06-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="3df06-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="3df06-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-176">Dá suporte a mídia removível</span><span class="sxs-lookup"><span data-stu-id="3df06-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="3df06-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="3df06-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="3df06-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="3df06-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="3df06-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="3df06-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="3df06-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="3df06-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-181">Dá suporte à mídia Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="3df06-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="3df06-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="3df06-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-183">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3df06-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-184">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3df06-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-186">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="3df06-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-187">Matriz de explicações mais detalhadas para qualquer um dos recursos do dispositivo de acesso indicados na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="3df06-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="3df06-188">Cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="3df06-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="3df06-189">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-190">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3df06-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-193">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3df06-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-194">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="3df06-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="3df06-195">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-196">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3df06-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-199">Algoritmo ou ferramenta usada pelo dispositivo para dar suporte à compactação.</span><span class="sxs-lookup"><span data-stu-id="3df06-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="3df06-200">Se não for possível ou não desejar descrever o esquema de compactação (talvez porque não seja conhecido), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o dispositivo dá suporte a recursos de compactação; "Compactado" para representar que o dispositivo dá suporte a recursos de compactação, mas seu esquema de compactação não é conhecido ou não é divulgado; e "não compactado" para representar que o dispositivo não oferece suporte a recursos de compactação.</span><span class="sxs-lookup"><span data-stu-id="3df06-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="3df06-201">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="3df06-202">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3df06-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="3df06-203">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="3df06-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="3df06-204">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="3df06-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3df06-205">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="3df06-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="3df06-206">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="3df06-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3df06-207">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="3df06-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-208">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3df06-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-209">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3df06-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-211">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3df06-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-212">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3df06-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="3df06-213">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3df06-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="3df06-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3df06-215"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="3df06-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-216">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3df06-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="3df06-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3df06-218">(1)</span><span class="sxs-lookup"><span data-stu-id="3df06-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-219">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3df06-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3df06-221">(2)</span><span class="sxs-lookup"><span data-stu-id="3df06-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3df06-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="3df06-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3df06-223">(3)</span><span class="sxs-lookup"><span data-stu-id="3df06-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-224">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="3df06-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3df06-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="3df06-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3df06-226">(4)</span><span class="sxs-lookup"><span data-stu-id="3df06-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-227">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-227">Device is not working properly.</span></span> <span data-ttu-id="3df06-228">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3df06-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3df06-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="3df06-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3df06-230">(5)</span><span class="sxs-lookup"><span data-stu-id="3df06-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-231">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="3df06-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3df06-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="3df06-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3df06-233"> (6)</span><span class="sxs-lookup"><span data-stu-id="3df06-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-234">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3df06-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3df06-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="3df06-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3df06-236">(7)</span><span class="sxs-lookup"><span data-stu-id="3df06-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3df06-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="3df06-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3df06-238">(8)</span><span class="sxs-lookup"><span data-stu-id="3df06-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-239">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="3df06-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3df06-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="3df06-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3df06-241">(9)</span><span class="sxs-lookup"><span data-stu-id="3df06-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-242">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-242">Device is not working properly.</span></span> <span data-ttu-id="3df06-243">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3df06-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="3df06-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3df06-245">(10)</span><span class="sxs-lookup"><span data-stu-id="3df06-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-246">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3df06-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="3df06-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3df06-248">(11)</span><span class="sxs-lookup"><span data-stu-id="3df06-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-249">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3df06-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="3df06-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3df06-251">12</span><span class="sxs-lookup"><span data-stu-id="3df06-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-252">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="3df06-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3df06-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3df06-254">(13)</span><span class="sxs-lookup"><span data-stu-id="3df06-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-255">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3df06-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="3df06-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3df06-257">(14)</span><span class="sxs-lookup"><span data-stu-id="3df06-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-258">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3df06-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3df06-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="3df06-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3df06-260">(15)</span><span class="sxs-lookup"><span data-stu-id="3df06-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-261">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="3df06-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3df06-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="3df06-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3df06-263">(16)</span><span class="sxs-lookup"><span data-stu-id="3df06-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-264">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="3df06-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3df06-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="3df06-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3df06-266">(17)</span><span class="sxs-lookup"><span data-stu-id="3df06-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-267">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3df06-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3df06-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3df06-269">(18)</span><span class="sxs-lookup"><span data-stu-id="3df06-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-270">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="3df06-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3df06-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="3df06-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3df06-272">(19)</span><span class="sxs-lookup"><span data-stu-id="3df06-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3df06-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="3df06-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3df06-274">(20)</span><span class="sxs-lookup"><span data-stu-id="3df06-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-275">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3df06-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3df06-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3df06-277">(21)</span><span class="sxs-lookup"><span data-stu-id="3df06-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-278">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="3df06-278">System failure.</span></span> <span data-ttu-id="3df06-279">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="3df06-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3df06-280">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3df06-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="3df06-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3df06-282">(22)</span><span class="sxs-lookup"><span data-stu-id="3df06-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-283">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3df06-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3df06-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="3df06-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3df06-285">(23)</span><span class="sxs-lookup"><span data-stu-id="3df06-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-286">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="3df06-286">System failure.</span></span> <span data-ttu-id="3df06-287">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="3df06-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3df06-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="3df06-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3df06-289">(24)</span><span class="sxs-lookup"><span data-stu-id="3df06-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-290">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="3df06-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3df06-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3df06-292">(25)</span><span class="sxs-lookup"><span data-stu-id="3df06-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-293">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3df06-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3df06-295">(26)</span><span class="sxs-lookup"><span data-stu-id="3df06-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-296">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3df06-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="3df06-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3df06-298">(27)</span><span class="sxs-lookup"><span data-stu-id="3df06-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-299">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="3df06-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3df06-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="3df06-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3df06-301">(28)</span><span class="sxs-lookup"><span data-stu-id="3df06-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-302">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="3df06-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3df06-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="3df06-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3df06-304">(29)</span><span class="sxs-lookup"><span data-stu-id="3df06-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-305">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3df06-305">Device is disabled.</span></span> <span data-ttu-id="3df06-306">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="3df06-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3df06-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="3df06-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3df06-308">(30)</span><span class="sxs-lookup"><span data-stu-id="3df06-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-309">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="3df06-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3df06-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3df06-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3df06-311">(31)</span><span class="sxs-lookup"><span data-stu-id="3df06-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-312">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-312">Device is not working properly.</span></span> <span data-ttu-id="3df06-313">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="3df06-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-314">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="3df06-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-315">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3df06-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-317">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3df06-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-318">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3df06-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3df06-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-320">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3df06-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-323">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3df06-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3df06-324">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="3df06-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3df06-325">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="3df06-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="3df06-326">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-327">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="3df06-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-328">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3df06-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-330">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3df06-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-331">Tamanho de bloco padrão, em bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="3df06-332">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3df06-333">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3df06-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-334">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3df06-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-337">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="3df06-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-338">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="3df06-338">Description of the object.</span></span>

<span data-ttu-id="3df06-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-340">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3df06-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-343">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| File Functions \| GetLogicalDriveStrings")</span><span class="sxs-lookup"><span data-stu-id="3df06-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-344">Identificador exclusivo de uma unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3df06-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="3df06-345">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-346">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="3df06-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-349">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="3df06-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-350">Letra da unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3df06-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="3df06-351">Exemplo: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="3df06-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="3df06-352">**DriveIntegrity**</span><span class="sxs-lookup"><span data-stu-id="3df06-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-353">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3df06-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-355">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3df06-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-356">Se **for true**, os arquivos poderão ser lidos com precisão do dispositivo de CD.</span><span class="sxs-lookup"><span data-stu-id="3df06-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="3df06-357">Isso é feito lendo um bloco de dados duas vezes e comparando os dados contra si mesmo.</span><span class="sxs-lookup"><span data-stu-id="3df06-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-358">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3df06-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-359">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3df06-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-361">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="3df06-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="3df06-362">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3df06-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-366">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="3df06-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="3df06-367">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-368">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="3df06-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-369">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-371">Tipo de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="3df06-372">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-373">**FileSystemFlags**</span><span class="sxs-lookup"><span data-stu-id="3df06-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-374">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-376">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções do sistema de arquivos \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="3df06-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-377">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="3df06-377">This property is obsolete.</span></span> <span data-ttu-id="3df06-378">No lugar dessa propriedade, use **FileSystemFlagsEx**.</span><span class="sxs-lookup"><span data-stu-id="3df06-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-379">**FileSystemFlagsEx**</span><span class="sxs-lookup"><span data-stu-id="3df06-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-380">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3df06-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-382">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções do sistema de arquivos \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="3df06-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-383">Sinalizadores do sistema de arquivos associados à unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="3df06-384">Esse parâmetro pode ser qualquer combinação de sinalizadores, mas **a \_ \_ compactação de arquivo FS** e o Vol. de **FS são \_ \_ \_ compactados** são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="3df06-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="3df06-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Pesquisa com distinção de maiúsculas e minúsculas** (1)</span><span class="sxs-lookup"><span data-stu-id="3df06-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-386">O sistema de arquivos dá suporte a nomes de arquivos que diferenciam maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="3df06-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="3df06-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Nomes preservados de caso** (2)</span><span class="sxs-lookup"><span data-stu-id="3df06-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-388">O sistema de arquivos preserva o caso de nomes de arquivo quando ele coloca um nome em um disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="3df06-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode em disco** (4)</span><span class="sxs-lookup"><span data-stu-id="3df06-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-390">O sistema de arquivos dá suporte a Unicode em nomes de arquivo conforme eles aparecem no disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="3df06-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**ACLs persistentes** (8)</span><span class="sxs-lookup"><span data-stu-id="3df06-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-392">O sistema de arquivos preserva e impõe listas de controle de acesso (ACLs).</span><span class="sxs-lookup"><span data-stu-id="3df06-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="3df06-393">Por exemplo, o sistema de arquivos NTFS preserva e impõe ACLs e o sistema de arquivos FAT não.</span><span class="sxs-lookup"><span data-stu-id="3df06-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="3df06-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Compactação de arquivo** (16)</span><span class="sxs-lookup"><span data-stu-id="3df06-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-395">O sistema de arquivos dá suporte à compactação baseada em arquivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="3df06-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Cotas de volume** (32)</span><span class="sxs-lookup"><span data-stu-id="3df06-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-397">O sistema de arquivos dá suporte a cotas de disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="3df06-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Dá suporte a arquivos esparsos** (64)</span><span class="sxs-lookup"><span data-stu-id="3df06-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-399">O sistema de arquivos dá suporte a arquivos sobressalentes.</span><span class="sxs-lookup"><span data-stu-id="3df06-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="3df06-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Dá suporte a pontos de nova análise** (128)</span><span class="sxs-lookup"><span data-stu-id="3df06-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-401">O sistema de arquivos dá suporte a pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="3df06-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="3df06-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Dá suporte ao armazenamento remoto** (256)</span><span class="sxs-lookup"><span data-stu-id="3df06-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-403">O sistema de arquivos dá suporte ao armazenamento remoto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3df06-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="3df06-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Dá suporte a nomes longos** (16384)</span><span class="sxs-lookup"><span data-stu-id="3df06-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-405">O sistema de arquivos dá suporte a nomes de arquivos com mais de oito caracteres.</span><span class="sxs-lookup"><span data-stu-id="3df06-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="3df06-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>O **volume está compactado** (32768)</span><span class="sxs-lookup"><span data-stu-id="3df06-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-407">O volume de disco especificado é um volume compactado, por exemplo, um volume do DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="3df06-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="3df06-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Volume somente leitura** (524289)</span><span class="sxs-lookup"><span data-stu-id="3df06-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-409">O volume especificado é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3df06-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="3df06-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Dá suporte a IDs de objeto** (65536)</span><span class="sxs-lookup"><span data-stu-id="3df06-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-411">O sistema de arquivos dá suporte a identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="3df06-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="3df06-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Dá suporte à criptografia** (131072)</span><span class="sxs-lookup"><span data-stu-id="3df06-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-413">O sistema de arquivos dá suporte ao EFS (sistema de arquivos criptografados).</span><span class="sxs-lookup"><span data-stu-id="3df06-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="3df06-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Dá suporte a fluxos nomeados** (262144)</span><span class="sxs-lookup"><span data-stu-id="3df06-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-415">O sistema de arquivos dá suporte a fluxos nomeados.</span><span class="sxs-lookup"><span data-stu-id="3df06-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="3df06-416">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="3df06-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3df06-417">**Id**</span><span class="sxs-lookup"><span data-stu-id="3df06-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-420">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="3df06-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-421">Letra da unidade que identifica exclusivamente esta unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3df06-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="3df06-422">Exemplo: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="3df06-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="3df06-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3df06-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-424">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3df06-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-426">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="3df06-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-427">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3df06-427">Date and time the object is installed.</span></span> <span data-ttu-id="3df06-428">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3df06-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3df06-429">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-430">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3df06-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-431">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3df06-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-433">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3df06-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3df06-434">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-435">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="3df06-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-438">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="3df06-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-439">Fabricante da unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="3df06-440">Exemplo: "PLEXTOR"</span><span class="sxs-lookup"><span data-stu-id="3df06-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="3df06-441">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3df06-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-442">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3df06-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-444">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3df06-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-445">Tamanho máximo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="3df06-446">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3df06-447">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3df06-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-448">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="3df06-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-449">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3df06-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-451">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções do sistema de arquivos \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="3df06-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-452">Comprimento máximo de um componente de nome de arquivo suportado pela unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="3df06-453">Um componente de nome de arquivo a parte de um nome de arquivo entre barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="3df06-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="3df06-454">O valor pode ser usado para indicar que nomes longos têm suporte pelo sistema de arquivos especificado.</span><span class="sxs-lookup"><span data-stu-id="3df06-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="3df06-455">Por exemplo, para um sistema de arquivos FAT com suporte a nomes longos, a função armazena o valor 255, em vez do indicador de 8,3 anterior.</span><span class="sxs-lookup"><span data-stu-id="3df06-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="3df06-456">Os nomes longos também podem ter suporte em sistemas que usam o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="3df06-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="3df06-457">Exemplo: 255</span><span class="sxs-lookup"><span data-stu-id="3df06-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="3df06-458">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="3df06-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-459">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3df06-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-461">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="3df06-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-462">Tamanho máximo, em quilobytes, de mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="3df06-463">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3df06-464">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3df06-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-465">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="3df06-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-466">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3df06-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-468">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções do sistema de arquivos \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="3df06-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-469">Se for **true**, um CD-ROM estará na unidade.</span><span class="sxs-lookup"><span data-stu-id="3df06-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-470">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="3df06-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-471">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-473">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="3df06-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-474">Tipo de mídia que pode ser usada ou acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="3df06-475">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="3df06-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="3df06-476">**Acesso aleatório** ("acesso aleatório")</span><span class="sxs-lookup"><span data-stu-id="3df06-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="3df06-477">**Dá suporte à gravação** ("dá suporte à gravação")</span><span class="sxs-lookup"><span data-stu-id="3df06-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="3df06-478">**Mídia removível** ("mídia removível")</span><span class="sxs-lookup"><span data-stu-id="3df06-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="3df06-479">**CD-ROM** ("CD-ROM")</span><span class="sxs-lookup"><span data-stu-id="3df06-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-480">**MfrAssignedRevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="3df06-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-483">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK \| KernelModeDrivers \| [**Storage \_ Device \_ DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="3df06-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-484">Nível de revisão de firmware atribuído pelo fabricante.</span><span class="sxs-lookup"><span data-stu-id="3df06-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-485">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3df06-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-486">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3df06-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-488">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3df06-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-489">Tamanho mínimo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="3df06-490">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3df06-491">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3df06-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-492">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3df06-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-493">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-494">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-495">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3df06-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-496">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="3df06-496">Label for the object.</span></span> <span data-ttu-id="3df06-497">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="3df06-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3df06-498">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-499">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="3df06-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-500">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3df06-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-501">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-502">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="3df06-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="3df06-503">Se a limpeza manual ou automática for possível, ela será indicada na propriedade **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="3df06-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="3df06-504">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-505">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="3df06-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-506">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3df06-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-508">Número máximo de mídias que podem ser suportadas ou inseridas, quando o dispositivo de acesso à mídia dá suporte a várias mídias individuais.</span><span class="sxs-lookup"><span data-stu-id="3df06-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="3df06-509">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3df06-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-511">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-513">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3df06-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-514">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3df06-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3df06-515">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3df06-516">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3df06-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3df06-517">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3df06-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-518">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3df06-519">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-520">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3df06-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3df06-521">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="3df06-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3df06-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3df06-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3df06-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3df06-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-524">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3df06-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3df06-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3df06-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3df06-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3df06-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-527">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3df06-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3df06-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="3df06-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-529">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="3df06-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3df06-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="3df06-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-531">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="3df06-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3df06-532">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="3df06-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="3df06-533">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="3df06-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3df06-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="3df06-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-535">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="3df06-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3df06-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="3df06-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3df06-537">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="3df06-537">Timed Power-On Supported</span></span>

<span data-ttu-id="3df06-538">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="3df06-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-539">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3df06-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-540">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3df06-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-541">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df06-542">Se **for true**, o dispositivo poderá ser gerenciado por energia, o que significa que ele pode ser colocado no modo de suspensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3df06-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="3df06-543">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="3df06-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3df06-544">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-545">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="3df06-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-546">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-547">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-548">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| RevisionLevel")</span><span class="sxs-lookup"><span data-stu-id="3df06-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-549">Nível de revisão de firmware da unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="3df06-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-551">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3df06-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-552">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-553">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| SCSI estruturas \| [**SCSI \_ solicitação \_**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| PathId")</span><span class="sxs-lookup"><span data-stu-id="3df06-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-554">Número de barramento SCSI para a unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="3df06-555">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="3df06-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3df06-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="3df06-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-557">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-558">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-559">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| SCSI estruturas SCSI \| [**\_ Request \_**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| LUN")</span><span class="sxs-lookup"><span data-stu-id="3df06-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-560">LUN (número de unidade lógica) SCSI da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="3df06-561">O LUN é usado para designar qual controlador SCSI está sendo acessado em um sistema com mais de um controlador sendo usado.</span><span class="sxs-lookup"><span data-stu-id="3df06-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="3df06-562">O identificador de dispositivo SCSI é semelhante, mas é a designação para vários dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="3df06-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="3df06-563">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="3df06-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3df06-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="3df06-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-565">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-566">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-567">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| SCSI estruturas SCSI \| [**\_ Request \_**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ScsiStatus")</span><span class="sxs-lookup"><span data-stu-id="3df06-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-568">Número da porta SCSI da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="3df06-569">Example: 1</span><span class="sxs-lookup"><span data-stu-id="3df06-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="3df06-570">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="3df06-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-571">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-572">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-573">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| DeviceIoControl \| IOCTL \_ SCSI \_ Get \_ endereço")</span><span class="sxs-lookup"><span data-stu-id="3df06-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-574">Número de identificador SCSI da unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="3df06-575">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="3df06-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3df06-576">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3df06-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-577">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-578">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-579">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estruturas de entrada e saída de dispositivo win32api \| [**\_ \_ descritor de dispositivo de armazenamento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="3df06-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-580">Número fornecido pelo fabricante que identifica a mídia física.</span><span class="sxs-lookup"><span data-stu-id="3df06-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="3df06-581">Exemplo: WD-WM3493798728.</span><span class="sxs-lookup"><span data-stu-id="3df06-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-582">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="3df06-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-583">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3df06-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-584">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-585">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções de arquivo \| GetDiskFreeSpace"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3df06-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-586">Tamanho da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="3df06-586">Size of the disk drive.</span></span>

<span data-ttu-id="3df06-587">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3df06-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-588">**Status**</span><span class="sxs-lookup"><span data-stu-id="3df06-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-589">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-590">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-591">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3df06-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-592">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3df06-592">Current status of the object.</span></span> <span data-ttu-id="3df06-593">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="3df06-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3df06-594">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="3df06-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3df06-595">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="3df06-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3df06-596">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="3df06-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3df06-597">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="3df06-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3df06-598">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3df06-599">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3df06-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3df06-600">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3df06-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3df06-601">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="3df06-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3df06-602">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3df06-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3df06-603">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3df06-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3df06-604">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3df06-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3df06-605">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="3df06-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3df06-606">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="3df06-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3df06-607">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="3df06-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3df06-608">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="3df06-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3df06-609">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3df06-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3df06-610">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="3df06-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3df06-611">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="3df06-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3df06-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-613">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df06-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-614">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-615">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="3df06-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-616">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3df06-616">State of the logical device.</span></span> <span data-ttu-id="3df06-617">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="3df06-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3df06-618">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3df06-619">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3df06-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3df06-620">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3df06-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3df06-621">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3df06-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3df06-622">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="3df06-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3df06-623">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="3df06-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3df06-624">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3df06-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-625">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-626">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-627">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3df06-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3df06-628">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="3df06-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="3df06-629">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-630">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3df06-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-631">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-632">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-633">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3df06-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3df06-634">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="3df06-634">Name of the scoping system.</span></span>

<span data-ttu-id="3df06-635">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3df06-636">**Transferível**</span><span class="sxs-lookup"><span data-stu-id="3df06-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-637">Tipo de dados: **real64**</span><span class="sxs-lookup"><span data-stu-id="3df06-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-638">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-639">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| referência de arquivo win32api e referência de hora"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes por segundo")</span><span class="sxs-lookup"><span data-stu-id="3df06-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-640">Taxa de transferência da unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3df06-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="3df06-641">Um valor de-1 indica que a taxa não pode ser determinada.</span><span class="sxs-lookup"><span data-stu-id="3df06-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="3df06-642">Quando isso acontece, o CD não está na unidade.</span><span class="sxs-lookup"><span data-stu-id="3df06-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-643">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="3df06-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-644">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-645">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-646">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções do sistema de arquivos \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="3df06-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-647">Nome do volume da unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="3df06-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="3df06-648">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3df06-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df06-649">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3df06-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df06-650">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3df06-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df06-651">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api de \| funções do sistema de arquivos \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="3df06-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="3df06-652">Número de série de volume da mídia na unidade de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3df06-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="3df06-653">Exemplo: A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="3df06-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3df06-654">Comentários</span><span class="sxs-lookup"><span data-stu-id="3df06-654">Remarks</span></span>

<span data-ttu-id="3df06-655">A classe **Win32 \_ CDROMDrive** é derivada de [**\_ CDROMDrive CIM**](cim-cdromdrive.md) que deriva do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="3df06-656">A classe **CIM \_ MediaAccessDevice** deriva do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3df06-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3df06-657">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3df06-657">Examples</span></span>

<span data-ttu-id="3df06-658">O exemplo de VBScript a seguir determina se um CD está em uma unidade de CDROM.</span><span class="sxs-lookup"><span data-stu-id="3df06-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="3df06-659">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df06-659">Requirements</span></span>



| <span data-ttu-id="3df06-660">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df06-660">Requirement</span></span> | <span data-ttu-id="3df06-661">Valor</span><span class="sxs-lookup"><span data-stu-id="3df06-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3df06-662">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df06-662">Minimum supported client</span></span><br/> | <span data-ttu-id="3df06-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3df06-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3df06-664">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df06-664">Minimum supported server</span></span><br/> | <span data-ttu-id="3df06-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3df06-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3df06-666">Namespace</span><span class="sxs-lookup"><span data-stu-id="3df06-666">Namespace</span></span><br/>                | <span data-ttu-id="3df06-667">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3df06-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3df06-668">MOF</span><span class="sxs-lookup"><span data-stu-id="3df06-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3df06-669"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3df06-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3df06-670">DLL</span><span class="sxs-lookup"><span data-stu-id="3df06-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df06-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df06-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df06-672">Confira também</span><span class="sxs-lookup"><span data-stu-id="3df06-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df06-673">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3df06-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="3df06-674">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="3df06-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3df06-675">Tarefas do WMI: hardware do computador</span><span class="sxs-lookup"><span data-stu-id="3df06-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="3df06-676">Tarefas do WMI: discos e sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="3df06-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

