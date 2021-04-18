---
description: Representa uma fonte de dados que é resolvida para um dispositivo de armazenamento local real em um sistema de computador que executa o Windows.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752954"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="8b671-103">Classe do disco lógico do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="8b671-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="8b671-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) do **\_ LogicalDisk do Win32** representa uma fonte de dados que resolve para um dispositivo de armazenamento local real em um sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="8b671-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="8b671-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8b671-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8b671-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8b671-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b671-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b671-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
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
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
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
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="8b671-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8b671-108">Members</span></span>

<span data-ttu-id="8b671-109">A classe do disco **\_ lógico do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8b671-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="8b671-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b671-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b671-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b671-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b671-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b671-112">Methods</span></span>

<span data-ttu-id="8b671-113">A classe do disco **\_ lógico do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8b671-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="8b671-114">Método</span><span class="sxs-lookup"><span data-stu-id="8b671-114">Method</span></span>                                                                             | <span data-ttu-id="8b671-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b671-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b671-116">**Chkdsk**</span><span class="sxs-lookup"><span data-stu-id="8b671-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="8b671-117">Invoca a operação [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) no disco.</span><span class="sxs-lookup"><span data-stu-id="8b671-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8b671-118">**ExcludeFromAutochk**</span><span class="sxs-lookup"><span data-stu-id="8b671-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="8b671-119">Exclui discos da operação [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) a ser executada na próxima reinicialização.</span><span class="sxs-lookup"><span data-stu-id="8b671-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="8b671-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="8b671-120">**Reset**</span></span>                                                                          | <span data-ttu-id="8b671-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="8b671-121">Not implemented.</span></span> <span data-ttu-id="8b671-122">Para obter mais informações sobre como implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**\_ LogicalDisk do CIM**](cim-logicaldisk.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="8b671-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="8b671-123">**ScheduleAutoChk**</span><span class="sxs-lookup"><span data-stu-id="8b671-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="8b671-124">Agenda o [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) a ser executado na próxima reinicialização se o bit sujo tiver sido definido.</span><span class="sxs-lookup"><span data-stu-id="8b671-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="8b671-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8b671-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="8b671-126">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="8b671-126">Not implemented.</span></span> <span data-ttu-id="8b671-127">Para obter mais informações sobre como implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**\_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="8b671-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8b671-128">Properties</span></span>

<span data-ttu-id="8b671-129">A classe do disco **\_ lógico do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b671-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b671-130">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="8b671-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b671-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-133">Tipo de acesso à mídia disponível.</span><span class="sxs-lookup"><span data-stu-id="8b671-133">Type of media access available.</span></span>

<span data-ttu-id="8b671-134">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b671-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b671-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="8b671-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="8b671-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="8b671-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="8b671-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-138">Gravável</span><span class="sxs-lookup"><span data-stu-id="8b671-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="8b671-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="8b671-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="8b671-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="8b671-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-141">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="8b671-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-142">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b671-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="8b671-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-145">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-145">Availability and status of the device.</span></span>

<span data-ttu-id="8b671-146">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8b671-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8b671-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b671-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8b671-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8b671-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="8b671-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-150">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="8b671-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8b671-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="8b671-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8b671-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="8b671-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8b671-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="8b671-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8b671-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="8b671-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8b671-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="8b671-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-156">Offline</span><span class="sxs-lookup"><span data-stu-id="8b671-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8b671-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="8b671-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8b671-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="8b671-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8b671-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="8b671-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8b671-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="8b671-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8b671-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="8b671-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-162">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8b671-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8b671-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="8b671-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-164">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="8b671-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8b671-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="8b671-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-166">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8b671-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="8b671-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8b671-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="8b671-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-169">O dispositivo está em um estado de aviso, mas também em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="8b671-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8b671-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="8b671-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-171">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="8b671-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8b671-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="8b671-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-173">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="8b671-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8b671-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="8b671-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-175">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="8b671-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8b671-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="8b671-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-177">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="8b671-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="8b671-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-179">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b671-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-181">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="8b671-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-182">Tamanho, em bytes, dos blocos que formam esta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b671-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="8b671-183">Se for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira 1.</span><span class="sxs-lookup"><span data-stu-id="8b671-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="8b671-184">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="8b671-185">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8b671-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-186">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8b671-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-189">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8b671-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-190">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="8b671-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="8b671-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-192">**Compactado**</span><span class="sxs-lookup"><span data-stu-id="8b671-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-193">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-195">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| File System Functions GetVolumeInformation o Vol. de sistema de arquivos \| [](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| \_ \_ é \_ compactado")</span><span class="sxs-lookup"><span data-stu-id="8b671-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-196">Se **for true**, o volume lógico existirá como uma única entidade compactada, como um volume do DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="8b671-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="8b671-197">Se a compactação baseada em arquivo tiver suporte, como no NTFS, essa propriedade será **false**.</span><span class="sxs-lookup"><span data-stu-id="8b671-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-198">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8b671-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-199">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b671-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-201">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8b671-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-202">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8b671-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="8b671-203">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8b671-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="8b671-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8b671-205"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="8b671-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-206">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8b671-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="8b671-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8b671-208">(1)</span><span class="sxs-lookup"><span data-stu-id="8b671-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-209">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8b671-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8b671-211">(2)</span><span class="sxs-lookup"><span data-stu-id="8b671-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8b671-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="8b671-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8b671-213">(3)</span><span class="sxs-lookup"><span data-stu-id="8b671-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-214">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="8b671-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8b671-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="8b671-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8b671-216">(4)</span><span class="sxs-lookup"><span data-stu-id="8b671-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-217">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-217">Device is not working properly.</span></span> <span data-ttu-id="8b671-218">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="8b671-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8b671-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="8b671-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8b671-220">(5)</span><span class="sxs-lookup"><span data-stu-id="8b671-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-221">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="8b671-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8b671-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="8b671-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8b671-223"> (6)</span><span class="sxs-lookup"><span data-stu-id="8b671-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-224">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8b671-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8b671-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="8b671-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8b671-226">(7)</span><span class="sxs-lookup"><span data-stu-id="8b671-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8b671-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="8b671-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8b671-228">(8)</span><span class="sxs-lookup"><span data-stu-id="8b671-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-229">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="8b671-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8b671-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="8b671-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8b671-231">(9)</span><span class="sxs-lookup"><span data-stu-id="8b671-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-232">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-232">Device is not working properly.</span></span> <span data-ttu-id="8b671-233">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8b671-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="8b671-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8b671-235">(10)</span><span class="sxs-lookup"><span data-stu-id="8b671-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-236">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8b671-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="8b671-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8b671-238">(11)</span><span class="sxs-lookup"><span data-stu-id="8b671-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-239">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8b671-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="8b671-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8b671-241">12</span><span class="sxs-lookup"><span data-stu-id="8b671-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-242">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="8b671-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8b671-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8b671-244">(13)</span><span class="sxs-lookup"><span data-stu-id="8b671-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-245">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8b671-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="8b671-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8b671-247">(14)</span><span class="sxs-lookup"><span data-stu-id="8b671-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-248">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="8b671-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8b671-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="8b671-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8b671-250">(15)</span><span class="sxs-lookup"><span data-stu-id="8b671-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-251">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="8b671-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8b671-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="8b671-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8b671-253">(16)</span><span class="sxs-lookup"><span data-stu-id="8b671-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-254">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="8b671-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8b671-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="8b671-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8b671-256">(17)</span><span class="sxs-lookup"><span data-stu-id="8b671-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-257">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8b671-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8b671-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8b671-259">(18)</span><span class="sxs-lookup"><span data-stu-id="8b671-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-260">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="8b671-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8b671-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="8b671-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8b671-262">(19)</span><span class="sxs-lookup"><span data-stu-id="8b671-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8b671-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="8b671-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8b671-264">(20)</span><span class="sxs-lookup"><span data-stu-id="8b671-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-265">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="8b671-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8b671-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8b671-267">(21)</span><span class="sxs-lookup"><span data-stu-id="8b671-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-268">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="8b671-268">System failure.</span></span> <span data-ttu-id="8b671-269">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="8b671-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8b671-270">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8b671-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="8b671-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8b671-272">(22)</span><span class="sxs-lookup"><span data-stu-id="8b671-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-273">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b671-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8b671-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="8b671-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8b671-275">(23)</span><span class="sxs-lookup"><span data-stu-id="8b671-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-276">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="8b671-276">System failure.</span></span> <span data-ttu-id="8b671-277">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="8b671-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8b671-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="8b671-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8b671-279">(24)</span><span class="sxs-lookup"><span data-stu-id="8b671-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-280">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="8b671-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8b671-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8b671-282">(25)</span><span class="sxs-lookup"><span data-stu-id="8b671-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-283">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8b671-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8b671-285">(26)</span><span class="sxs-lookup"><span data-stu-id="8b671-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-286">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b671-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8b671-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="8b671-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8b671-288">(27)</span><span class="sxs-lookup"><span data-stu-id="8b671-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-289">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="8b671-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8b671-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="8b671-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8b671-291">(28)</span><span class="sxs-lookup"><span data-stu-id="8b671-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-292">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="8b671-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8b671-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="8b671-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8b671-294">(29)</span><span class="sxs-lookup"><span data-stu-id="8b671-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-295">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b671-295">Device is disabled.</span></span> <span data-ttu-id="8b671-296">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="8b671-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8b671-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="8b671-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8b671-298">(30)</span><span class="sxs-lookup"><span data-stu-id="8b671-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-299">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="8b671-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8b671-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8b671-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8b671-301">(31)</span><span class="sxs-lookup"><span data-stu-id="8b671-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-302">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-302">Device is not working properly.</span></span> <span data-ttu-id="8b671-303">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="8b671-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-304">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8b671-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-305">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-307">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8b671-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-308">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8b671-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8b671-309">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-310">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b671-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-313">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8b671-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8b671-314">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="8b671-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8b671-315">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8b671-316">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-317">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8b671-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-320">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="8b671-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-321">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8b671-321">Description of the object.</span></span>

<span data-ttu-id="8b671-322">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-323">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8b671-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-326">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8b671-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-327">Identificador exclusivo do disco lógico de outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="8b671-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="8b671-328">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8b671-329">Para obter um exemplo de código que recupera essa propriedade, consulte a seção comentários, abaixo.</span><span class="sxs-lookup"><span data-stu-id="8b671-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="8b671-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b671-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| filefunctions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="8b671-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-334">Valor numérico que corresponde ao tipo de unidade de disco que este disco lógico representa.</span><span class="sxs-lookup"><span data-stu-id="8b671-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b671-335">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b671-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="8b671-336">**Nenhum diretório raiz** (1)</span><span class="sxs-lookup"><span data-stu-id="8b671-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="8b671-337">**Disco removível** (2)</span><span class="sxs-lookup"><span data-stu-id="8b671-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="8b671-338">**Disco local** (3)</span><span class="sxs-lookup"><span data-stu-id="8b671-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="8b671-339">**Unidade de rede** (4)</span><span class="sxs-lookup"><span data-stu-id="8b671-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="8b671-340">**CD** (5)</span><span class="sxs-lookup"><span data-stu-id="8b671-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="8b671-341">**Disco RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="8b671-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-342">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8b671-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-343">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-345">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="8b671-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="8b671-346">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8b671-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-350">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="8b671-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="8b671-351">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-352">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="8b671-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-355">Tipo de detecção de erro e correção com suporte nesta extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b671-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="8b671-356">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-357">**WPD**</span><span class="sxs-lookup"><span data-stu-id="8b671-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-358">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-360">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="8b671-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="8b671-361">Sistema de arquivos no disco lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-361">File system on the logical disk.</span></span>

<span data-ttu-id="8b671-362">Exemplo: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="8b671-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="8b671-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="8b671-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-364">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b671-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-366">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8b671-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-367">Espaço, em bytes, disponível no disco lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="8b671-368">Essa propriedade é herdada [**do \_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="8b671-369">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8b671-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8b671-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-371">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b671-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-373">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="8b671-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-374">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8b671-374">Date and time the object was installed.</span></span> <span data-ttu-id="8b671-375">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8b671-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8b671-376">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8b671-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-378">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b671-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-379">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-380">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8b671-381">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-382">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="8b671-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-383">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b671-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-385">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="8b671-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="8b671-386">Comprimento máximo de um componente de nome de arquivo suportado pela unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="8b671-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="8b671-387">Um componente de nome de arquivo é a parte de um nome de arquivo entre barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="8b671-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="8b671-388">O valor pode ser usado para indicar que nomes longos têm suporte pelo sistema de arquivos especificado.</span><span class="sxs-lookup"><span data-stu-id="8b671-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="8b671-389">Por exemplo, para um sistema de arquivos FAT com suporte a nomes longos, a função armazena o valor 255, em vez do indicador de 8,3 anterior.</span><span class="sxs-lookup"><span data-stu-id="8b671-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="8b671-390">Os nomes longos também podem ter suporte em sistemas que usam o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="8b671-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="8b671-391">Exemplo: 255</span><span class="sxs-lookup"><span data-stu-id="8b671-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="8b671-392">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="8b671-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-393">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b671-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-395">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de entrada e saída de dispositivo do win32api \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="8b671-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-396">Tipo de mídia atualmente presente na unidade lógica.</span><span class="sxs-lookup"><span data-stu-id="8b671-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="8b671-397">Esse valor será um dos valores da enumeração de tipo de mídia \_ definida em Winioctl. h.</span><span class="sxs-lookup"><span data-stu-id="8b671-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="8b671-398">O valor pode não ser exato para unidades removíveis, se atualmente não houver mídia na unidade.</span><span class="sxs-lookup"><span data-stu-id="8b671-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="8b671-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>O **formato é desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b671-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (1)</span><span class="sxs-lookup"><span data-stu-id="8b671-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-401">Disquete de 5 1/2 polegadas-1,2 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (2)</span><span class="sxs-lookup"><span data-stu-id="8b671-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-403">Disquete de 3 1/2 polegadas-1,44 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (3)</span><span class="sxs-lookup"><span data-stu-id="8b671-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-405">Disquete de 3 1/2 polegadas-2,88 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (4)</span><span class="sxs-lookup"><span data-stu-id="8b671-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-407">Disquete de 3 1/2 polegadas-20,8 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (5)</span><span class="sxs-lookup"><span data-stu-id="8b671-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-409">Disquete de 3 1/2 polegadas-720 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (6)</span><span class="sxs-lookup"><span data-stu-id="8b671-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-411">Disquete de 5 1/2 polegadas-360 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (7)</span><span class="sxs-lookup"><span data-stu-id="8b671-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-413">Disquete de 5 1/2 polegadas-320 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (8)</span><span class="sxs-lookup"><span data-stu-id="8b671-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-415">Disquete de 5 1/2 polegadas-320 KB-1024 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (9)</span><span class="sxs-lookup"><span data-stu-id="8b671-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-417">Disquete de 5 1/2 polegadas-180 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (10)</span><span class="sxs-lookup"><span data-stu-id="8b671-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-419">Disquete de 5 1/2 polegadas-160 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="8b671-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Mídia removível diferente do disquete** (11)</span><span class="sxs-lookup"><span data-stu-id="8b671-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="8b671-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Mídia de disco rígido fixa** (12)</span><span class="sxs-lookup"><span data-stu-id="8b671-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (13)</span><span class="sxs-lookup"><span data-stu-id="8b671-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-423">Disquete de 3 1/2 polegadas-120 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (14)</span><span class="sxs-lookup"><span data-stu-id="8b671-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-425">Disquete de 3 1/2 polegadas-640 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (15)</span><span class="sxs-lookup"><span data-stu-id="8b671-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-427">Disquete de 5 1/2 polegadas-640 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (16)</span><span class="sxs-lookup"><span data-stu-id="8b671-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-429">Disquete de 5 1/2 polegadas-720 KB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (17)</span><span class="sxs-lookup"><span data-stu-id="8b671-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-431">Disquete de 3 1/2 polegadas-1,2 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (18)</span><span class="sxs-lookup"><span data-stu-id="8b671-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-433">Disquete de 3 1/2 polegadas-1,23 MB-1024 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 polegadas** (19)</span><span class="sxs-lookup"><span data-stu-id="8b671-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-435">Disquete de 5 1/2 polegadas-1,23 MB-1024 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (20)</span><span class="sxs-lookup"><span data-stu-id="8b671-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-437">Disquete de 3 1/2 polegadas-128 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 polegadas** (21)</span><span class="sxs-lookup"><span data-stu-id="8b671-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-439">Disquete de 3 1/2 polegadas-230 MB-512 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="8b671-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**disquete de 8 polegadas** (22)</span><span class="sxs-lookup"><span data-stu-id="8b671-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-441">Disquete de 8 polegadas-256 KB-128 bytes/setor</span><span class="sxs-lookup"><span data-stu-id="8b671-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-442">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8b671-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-445">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8b671-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-446">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8b671-446">Label by which the object is known.</span></span> <span data-ttu-id="8b671-447">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="8b671-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8b671-448">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="8b671-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-450">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b671-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-452">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="8b671-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-453">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b671-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="8b671-454">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8b671-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="8b671-455">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b671-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="8b671-456">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="8b671-457">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8b671-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8b671-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-459">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-461">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8b671-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-462">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="8b671-463">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8b671-464">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8b671-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="8b671-465">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8b671-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-466">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b671-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b671-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-468">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8b671-469">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="8b671-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b671-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b671-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8b671-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="8b671-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8b671-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8b671-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8b671-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8b671-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-474">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8b671-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8b671-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="8b671-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-476">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="8b671-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8b671-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="8b671-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-478">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="8b671-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8b671-479">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="8b671-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="8b671-480">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="8b671-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8b671-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="8b671-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-482">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="8b671-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8b671-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="8b671-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8b671-484">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="8b671-484">Timed Power-On Supported</span></span>

<span data-ttu-id="8b671-485">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="8b671-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-486">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8b671-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-487">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-489">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="8b671-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="8b671-490">Essa propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="8b671-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="8b671-491">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="8b671-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-493">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-494">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-495">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| WNetGetConnection funções de rede do Windows \| ")</span><span class="sxs-lookup"><span data-stu-id="8b671-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-496">Caminho de rede para o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-497">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="8b671-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-498">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-500">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="8b671-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="8b671-501">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-502">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="8b671-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-503">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-505">Indica que o gerenciamento de cotas não está habilitado (TRUE) neste sistema.</span><span class="sxs-lookup"><span data-stu-id="8b671-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-506">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="8b671-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-507">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-508">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-509">Indica que o gerenciamento de cota foi usado, mas foi desabilitado (**true**).</span><span class="sxs-lookup"><span data-stu-id="8b671-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="8b671-510">Incompleto refere-se às informações deixadas no sistema de arquivos após o gerenciamento de cotas ter sido desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b671-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-511">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="8b671-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-512">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-514">Se **for true**, indica que o sistema de arquivos está no processo ativo de compilação de informações e configuração do disco para o gerenciamento de cotas.</span><span class="sxs-lookup"><span data-stu-id="8b671-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-515">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="8b671-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-516">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-517">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-518">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8b671-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-519">Tamanho da unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="8b671-519">Size of the disk drive.</span></span>

<span data-ttu-id="8b671-520">Essa propriedade é herdada [**do \_ LogicalDisk CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="8b671-521">Para obter um exemplo de código que recupera essa propriedade, consulte a seção comentários, abaixo.</span><span class="sxs-lookup"><span data-stu-id="8b671-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="8b671-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-525">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8b671-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-526">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8b671-526">Current status of the object.</span></span> <span data-ttu-id="8b671-527">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="8b671-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8b671-528">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8b671-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8b671-529">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8b671-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8b671-530">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8b671-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8b671-531">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8b671-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8b671-532">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8b671-533">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8b671-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8b671-534">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8b671-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8b671-535">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="8b671-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8b671-536">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8b671-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b671-537">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8b671-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8b671-538">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8b671-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8b671-539">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8b671-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8b671-540">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="8b671-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8b671-541">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="8b671-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8b671-542">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="8b671-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8b671-543">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8b671-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8b671-544">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="8b671-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8b671-545">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="8b671-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8b671-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-547">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b671-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-549">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="8b671-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-550">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-550">State of the logical device.</span></span> <span data-ttu-id="8b671-551">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="8b671-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8b671-552">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8b671-553">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8b671-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8b671-554">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="8b671-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8b671-555">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8b671-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8b671-556">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="8b671-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8b671-557">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="8b671-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8b671-558">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="8b671-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-559">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-560">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b671-561">Se **for true**, esse volume dará suporte a cotas de disco.</span><span class="sxs-lookup"><span data-stu-id="8b671-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-562">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="8b671-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-563">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-564">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-565">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ \_ Compact File Compression")</span><span class="sxs-lookup"><span data-stu-id="8b671-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-566">Se for **true**, a partição de disco lógico dará suporte à compactação baseada em arquivo, como é o caso com o sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="8b671-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="8b671-567">Essa propriedade será **falsa** quando a propriedade **compactada** for **true**.</span><span class="sxs-lookup"><span data-stu-id="8b671-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-568">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b671-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-569">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-570">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-571">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8b671-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8b671-572">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="8b671-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="8b671-573">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-574">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8b671-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-575">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-576">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-577">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8b671-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8b671-578">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="8b671-578">Name of the scoping system.</span></span>

<span data-ttu-id="8b671-579">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b671-580">**VolumeDirty**</span><span class="sxs-lookup"><span data-stu-id="8b671-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-581">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="8b671-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-582">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-583">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("fsctl \_ tem \_ volume \_ sujo")</span><span class="sxs-lookup"><span data-stu-id="8b671-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="8b671-584">Se **for true**, o disco exigirá que [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) seja executado na próxima reinicialização.</span><span class="sxs-lookup"><span data-stu-id="8b671-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="8b671-585">Essa propriedade só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador.</span><span class="sxs-lookup"><span data-stu-id="8b671-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="8b671-586">Ele não é aplicável a unidades lógicas mapeadas.</span><span class="sxs-lookup"><span data-stu-id="8b671-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-587">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="8b671-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-588">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-589">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8b671-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8b671-590">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="8b671-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="8b671-591">Nome do volume do disco lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="8b671-592">Restrições: no máximo 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8b671-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="8b671-593">Para obter um exemplo de código que recupera essa propriedade, consulte a seção comentários, abaixo.</span><span class="sxs-lookup"><span data-stu-id="8b671-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="8b671-594">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8b671-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b671-595">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8b671-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b671-596">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8b671-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b671-597">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções do sistema de arquivos win32api [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="8b671-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="8b671-598">Número de série de volume do disco lógico.</span><span class="sxs-lookup"><span data-stu-id="8b671-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="8b671-599">Restrições: máximo de 11 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8b671-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="8b671-600">Exemplo: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="8b671-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b671-601">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b671-601">Remarks</span></span>

<span data-ttu-id="8b671-602">A classe do disco **\_ lógico do Win32** é derivada do [**\_ LogicalDisk CIM**](cim-logicaldisk.md) que deriva do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="8b671-603">A classe **CIM \_ StorageExtent** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8b671-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8b671-604">Uma unidade de disco físico é a base de qualquer sistema de gerenciamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b671-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="8b671-605">No entanto, após a instalação de uma unidade de disco físico, nem os usuários nem administradores de sistema normalmente lidam com o hardware diretamente.</span><span class="sxs-lookup"><span data-stu-id="8b671-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="8b671-606">Em vez disso, os usuários e os administradores de sistema interagem com as unidades lógicas que foram criadas no disco.</span><span class="sxs-lookup"><span data-stu-id="8b671-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="8b671-607">Uma unidade lógica é uma subdivisão de uma partição que foi atribuída a sua própria letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="8b671-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="8b671-608">(É possível ter uma partição que não tenha sido atribuída a uma letra de unidade.) Quando você fala sobre a unidade C ou D, está se referindo a uma unidade lógica em vez de uma unidade de disco físico.</span><span class="sxs-lookup"><span data-stu-id="8b671-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="8b671-609">Da mesma forma, ao salvar um documento na unidade E, você o está salvando na unidade lógica.</span><span class="sxs-lookup"><span data-stu-id="8b671-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="8b671-610">Discos físicos compõem o hardware que compõe uma unidade, incluindo componentes como cabeçotes, setores e cilindros.</span><span class="sxs-lookup"><span data-stu-id="8b671-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="8b671-611">Unidades lógicas, por outro lado, têm propriedades como espaço em disco, espaço em disco disponível e letras de unidade.</span><span class="sxs-lookup"><span data-stu-id="8b671-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="8b671-612">A classe do **\_ LogicalDisk do Win32** pode ser usada apenas para enumerar as propriedades de unidades de disco locais.</span><span class="sxs-lookup"><span data-stu-id="8b671-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="8b671-613">No entanto, você pode usar a classe [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md) para enumerar as propriedades de unidades de rede mapeadas.</span><span class="sxs-lookup"><span data-stu-id="8b671-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8b671-614">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b671-614">Examples</span></span>

<span data-ttu-id="8b671-615">Você pode encontrar outros exemplos usando **o \_ LogicalDisk do Win32** para obter dados de disco ou volume no tópico [tarefas do WMI: discos e sistemas de arquivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .</span><span class="sxs-lookup"><span data-stu-id="8b671-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="8b671-616">O exemplo de código VBScript do [recuperador de informações do WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) na galeria do TechNet usa a classe do disco **\_ lógico do Win32** para recuperar informações de hardware de vários computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="8b671-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="8b671-617">[Obter informações de disco usando WMI/CIM...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) O exemplo de código do PowerShell na galeria do TechNet usa o **\_ LogicalDisk do Win32** para recuperar o **DeviceID**, o **VolumeName** e o **tamanho** de um dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="8b671-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="8b671-618">Em particular, este exemplo inclui manipulação de exceção rigorosa e retorna um único objeto por computador, em vez de por disco.</span><span class="sxs-lookup"><span data-stu-id="8b671-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="8b671-619">O script corporativo geralmente envolve a configuração de hardware e software em computadores remotos; por sua vez, isso exige que você conheça, antecipadamente, o tipo de unidades de disco instaladas em um computador.</span><span class="sxs-lookup"><span data-stu-id="8b671-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="8b671-620">Por exemplo, um script que instala um aplicativo na unidade E funciona somente se a unidade E for um disco rígido.</span><span class="sxs-lookup"><span data-stu-id="8b671-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="8b671-621">Se a unidade E representar um disquete ou uma unidade de CD-ROM, o script falhará.</span><span class="sxs-lookup"><span data-stu-id="8b671-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="8b671-622">O código a seguir identifica as unidades e os tipos de unidade instalados em um computador</span><span class="sxs-lookup"><span data-stu-id="8b671-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="8b671-623">Os exemplos a seguir enumeram o espaço livre em todas as unidades de disco rígido em um computador.</span><span class="sxs-lookup"><span data-stu-id="8b671-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="8b671-624">O exemplo de código a seguir retorna o tipo de sistema de arquivos (FAT, NTFS, FAT32 e assim por diante) usado em cada unidade em um computador.</span><span class="sxs-lookup"><span data-stu-id="8b671-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="8b671-625">O exemplo de código do PowerShell a seguir recupera informações adicionais sobre os discos locais lógicos.</span><span class="sxs-lookup"><span data-stu-id="8b671-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="8b671-626">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b671-626">Requirements</span></span>



| <span data-ttu-id="8b671-627">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b671-627">Requirement</span></span> | <span data-ttu-id="8b671-628">Valor</span><span class="sxs-lookup"><span data-stu-id="8b671-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b671-629">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b671-629">Minimum supported client</span></span><br/> | <span data-ttu-id="8b671-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b671-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b671-631">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b671-631">Minimum supported server</span></span><br/> | <span data-ttu-id="8b671-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b671-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b671-633">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b671-633">Namespace</span></span><br/>                | <span data-ttu-id="8b671-634">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8b671-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b671-635">MOF</span><span class="sxs-lookup"><span data-stu-id="8b671-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b671-636"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b671-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b671-637">DLL</span><span class="sxs-lookup"><span data-stu-id="8b671-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b671-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b671-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b671-639">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b671-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b671-640">**\_LOGICALDISK CIM**</span><span class="sxs-lookup"><span data-stu-id="8b671-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="8b671-641">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8b671-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8b671-642">Tarefas do WMI: discos e sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="8b671-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

