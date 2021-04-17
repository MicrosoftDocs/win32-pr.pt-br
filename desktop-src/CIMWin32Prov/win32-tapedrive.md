---
description: A \_ classe WMI TapeDrive do Win32 representa uma unidade de fita em um sistema de computador que executa o Windows. As unidades de fita são distinguidas principalmente pelo fato de que só podem ser acessadas em sequência.
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Classe Win32_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755838"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="b9800-104">\_Classe Win32 TapeDrive</span><span class="sxs-lookup"><span data-stu-id="b9800-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="b9800-105">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TapeDrive do Win32** representa uma unidade de fita em um sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="b9800-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="b9800-106">As unidades de fita são distinguidas principalmente pelo fato de que só podem ser acessadas em sequência.</span><span class="sxs-lookup"><span data-stu-id="b9800-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="b9800-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b9800-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b9800-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b9800-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9800-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9800-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="b9800-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b9800-110">Members</span></span>

<span data-ttu-id="b9800-111">A classe **Win32 \_ TapeDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b9800-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b9800-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9800-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9800-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9800-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9800-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9800-114">Methods</span></span>

<span data-ttu-id="b9800-115">A classe **Win32 \_ TapeDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b9800-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="b9800-116">Método</span><span class="sxs-lookup"><span data-stu-id="b9800-116">Method</span></span>            | <span data-ttu-id="b9800-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9800-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9800-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="b9800-118">**Reset**</span></span>         | <span data-ttu-id="b9800-119">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="b9800-119">Not implemented.</span></span> <span data-ttu-id="b9800-120">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="b9800-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b9800-121">**SetPowerState**</span></span> | <span data-ttu-id="b9800-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="b9800-122">Not implemented.</span></span> <span data-ttu-id="b9800-123">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b9800-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9800-124">Properties</span></span>

<span data-ttu-id="b9800-125">A classe **Win32 \_ TapeDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b9800-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9800-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="b9800-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9800-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-129">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b9800-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-130">Availability and status of the device.</span></span>

<span data-ttu-id="b9800-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9800-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b9800-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9800-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b9800-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b9800-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b9800-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-135">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="b9800-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b9800-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b9800-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b9800-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="b9800-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b9800-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="b9800-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b9800-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="b9800-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b9800-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="b9800-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b9800-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="b9800-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b9800-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="b9800-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b9800-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="b9800-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b9800-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="b9800-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b9800-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="b9800-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-146">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b9800-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b9800-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="b9800-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-148">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="b9800-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b9800-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="b9800-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-150">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b9800-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="b9800-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b9800-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b9800-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-153">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="b9800-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b9800-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b9800-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-155">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="b9800-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b9800-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b9800-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-157">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="b9800-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b9800-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="b9800-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-159">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="b9800-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b9800-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="b9800-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-161">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="b9800-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-162">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="b9800-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-163">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9800-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b9800-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-165">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="b9800-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-166">Matriz de recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="b9800-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="b9800-167">Por exemplo, o dispositivo pode dar suporte a acesso aleatório, mídia removível e limpeza automática.</span><span class="sxs-lookup"><span data-stu-id="b9800-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="b9800-168">Nesse caso, os valores 3, 7 e 9 seriam gravados na matriz.</span><span class="sxs-lookup"><span data-stu-id="b9800-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="b9800-169">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9800-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b9800-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9800-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b9800-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="b9800-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="b9800-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="b9800-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="b9800-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="b9800-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="b9800-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="b9800-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="b9800-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="b9800-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="b9800-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="b9800-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="b9800-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-178">Dá suporte a mídia removível</span><span class="sxs-lookup"><span data-stu-id="b9800-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="b9800-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="b9800-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="b9800-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="b9800-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="b9800-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="b9800-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="b9800-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="b9800-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-183">Dá suporte à mídia Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="b9800-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="b9800-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="b9800-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b9800-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-186">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b9800-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-188">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="b9800-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-189">Matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer recurso de dispositivo de acesso indicado na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="b9800-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="b9800-190">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="b9800-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="b9800-191">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-192">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b9800-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-195">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b9800-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-196">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b9800-196">Short description of the object.</span></span>

<span data-ttu-id="b9800-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-198">**Compactação**</span><span class="sxs-lookup"><span data-stu-id="b9800-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-199">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-201">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de backup em fita win32api \| [**fita \_ obter \_ \_ parâmetros de unidade**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| compactação")</span><span class="sxs-lookup"><span data-stu-id="b9800-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-202">Se for **true**, a compactação de dados de hardware será habilitada.</span><span class="sxs-lookup"><span data-stu-id="b9800-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b9800-203"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b9800-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b9800-204">FALSE</span><span class="sxs-lookup"><span data-stu-id="b9800-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b9800-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b9800-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b9800-206">TRUE</span><span class="sxs-lookup"><span data-stu-id="b9800-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b9800-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-210">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada pelo dispositivo para dar suporte à compactação.</span><span class="sxs-lookup"><span data-stu-id="b9800-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="b9800-211">Se não for possível ou não desejar descrever o esquema de compactação (talvez porque não seja conhecido), use as seguintes palavras: "desconhecido" para representar que não é conhecido se o dispositivo dá suporte a recursos de compactação ou não; "Compactado" para representar que o dispositivo dá suporte a recursos de compactação, mas seu esquema de compactação não é conhecido ou não é divulgado; e "não compactado" para representar que o dispositivo não oferece suporte a recursos de compactação.</span><span class="sxs-lookup"><span data-stu-id="b9800-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="b9800-212">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="b9800-213">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b9800-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b9800-214">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="b9800-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="b9800-215">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="b9800-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b9800-216">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="b9800-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="b9800-217">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="b9800-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b9800-218">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="b9800-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b9800-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-220">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-222">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b9800-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-223">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b9800-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b9800-224">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b9800-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="b9800-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b9800-226"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="b9800-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-227">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b9800-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="b9800-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b9800-229">(1)</span><span class="sxs-lookup"><span data-stu-id="b9800-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-230">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b9800-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b9800-232">(2)</span><span class="sxs-lookup"><span data-stu-id="b9800-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b9800-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="b9800-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b9800-234">(3)</span><span class="sxs-lookup"><span data-stu-id="b9800-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-235">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="b9800-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b9800-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="b9800-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b9800-237">(4)</span><span class="sxs-lookup"><span data-stu-id="b9800-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-238">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-238">Device is not working properly.</span></span> <span data-ttu-id="b9800-239">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b9800-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b9800-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="b9800-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b9800-241">(5)</span><span class="sxs-lookup"><span data-stu-id="b9800-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-242">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="b9800-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b9800-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="b9800-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b9800-244"> (6)</span><span class="sxs-lookup"><span data-stu-id="b9800-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-245">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b9800-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b9800-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="b9800-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b9800-247">(7)</span><span class="sxs-lookup"><span data-stu-id="b9800-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b9800-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="b9800-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b9800-249">(8)</span><span class="sxs-lookup"><span data-stu-id="b9800-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-250">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="b9800-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b9800-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="b9800-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b9800-252">(9)</span><span class="sxs-lookup"><span data-stu-id="b9800-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-253">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-253">Device is not working properly.</span></span> <span data-ttu-id="b9800-254">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b9800-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="b9800-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b9800-256">(10)</span><span class="sxs-lookup"><span data-stu-id="b9800-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-257">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b9800-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="b9800-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b9800-259">(11)</span><span class="sxs-lookup"><span data-stu-id="b9800-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-260">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b9800-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="b9800-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b9800-262">12</span><span class="sxs-lookup"><span data-stu-id="b9800-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-263">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="b9800-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b9800-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b9800-265">(13)</span><span class="sxs-lookup"><span data-stu-id="b9800-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-266">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b9800-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="b9800-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b9800-268">(14)</span><span class="sxs-lookup"><span data-stu-id="b9800-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-269">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="b9800-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b9800-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="b9800-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b9800-271">(15)</span><span class="sxs-lookup"><span data-stu-id="b9800-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-272">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="b9800-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b9800-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="b9800-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b9800-274">(16)</span><span class="sxs-lookup"><span data-stu-id="b9800-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-275">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="b9800-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b9800-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="b9800-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b9800-277">(17)</span><span class="sxs-lookup"><span data-stu-id="b9800-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-278">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b9800-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b9800-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b9800-280">(18)</span><span class="sxs-lookup"><span data-stu-id="b9800-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-281">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="b9800-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b9800-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="b9800-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b9800-283">(19)</span><span class="sxs-lookup"><span data-stu-id="b9800-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b9800-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="b9800-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b9800-285">(20)</span><span class="sxs-lookup"><span data-stu-id="b9800-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-286">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b9800-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b9800-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b9800-288">(21)</span><span class="sxs-lookup"><span data-stu-id="b9800-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-289">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="b9800-289">System failure.</span></span> <span data-ttu-id="b9800-290">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="b9800-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b9800-291">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b9800-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="b9800-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b9800-293">(22)</span><span class="sxs-lookup"><span data-stu-id="b9800-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-294">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b9800-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b9800-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="b9800-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b9800-296">(23)</span><span class="sxs-lookup"><span data-stu-id="b9800-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-297">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="b9800-297">System failure.</span></span> <span data-ttu-id="b9800-298">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="b9800-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b9800-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="b9800-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b9800-300">(24)</span><span class="sxs-lookup"><span data-stu-id="b9800-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-301">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="b9800-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b9800-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b9800-303">(25)</span><span class="sxs-lookup"><span data-stu-id="b9800-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-304">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b9800-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b9800-306">(26)</span><span class="sxs-lookup"><span data-stu-id="b9800-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-307">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b9800-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="b9800-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b9800-309">(27)</span><span class="sxs-lookup"><span data-stu-id="b9800-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-310">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="b9800-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b9800-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="b9800-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b9800-312">(28)</span><span class="sxs-lookup"><span data-stu-id="b9800-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-313">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="b9800-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b9800-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="b9800-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b9800-315">(29)</span><span class="sxs-lookup"><span data-stu-id="b9800-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-316">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b9800-316">Device is disabled.</span></span> <span data-ttu-id="b9800-317">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="b9800-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b9800-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="b9800-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b9800-319">(30)</span><span class="sxs-lookup"><span data-stu-id="b9800-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-320">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b9800-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b9800-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b9800-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b9800-322">(31)</span><span class="sxs-lookup"><span data-stu-id="b9800-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-323">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-323">Device is not working properly.</span></span> <span data-ttu-id="b9800-324">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="b9800-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-325">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b9800-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-326">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b9800-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-328">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b9800-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-329">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b9800-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b9800-330">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-331">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b9800-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-332">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-334">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b9800-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b9800-335">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b9800-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b9800-336">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b9800-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b9800-337">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-338">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="b9800-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-339">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9800-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-341">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b9800-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-342">Tamanho de bloco padrão, em bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="b9800-343">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b9800-344">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-345">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b9800-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-348">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b9800-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-349">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="b9800-349">Description of the object.</span></span>

<span data-ttu-id="b9800-350">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b9800-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-352">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-354">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| File Functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="b9800-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-355">Identificador exclusivo da unidade de fita com outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="b9800-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="b9800-356">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="b9800-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-358">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-360">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de backup em fita win32api \| [**fita \_ obter \_ \_ parâmetros de unidade**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ECC")</span><span class="sxs-lookup"><span data-stu-id="b9800-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-361">Se **for true**, o dispositivo dará suporte à correção de erro de hardware.</span><span class="sxs-lookup"><span data-stu-id="b9800-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="b9800-362">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="b9800-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="b9800-363">**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="b9800-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-364">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="b9800-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-365">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-367">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b9800-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-368">Tamanho da zona para o aviso de fim de fita (EOT).</span><span class="sxs-lookup"><span data-stu-id="b9800-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="b9800-369">Essa propriedade é herdada do [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-370">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b9800-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-371">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b9800-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-373">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="b9800-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b9800-374">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b9800-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-378">Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="b9800-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="b9800-379">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-380">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b9800-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-383">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="b9800-384">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-385">**FeaturesHigh**</span><span class="sxs-lookup"><span data-stu-id="b9800-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-386">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-388">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de backup em fita win32api \| [**fita \_ obter \_ \_ parâmetros de unidade**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesHigh")</span><span class="sxs-lookup"><span data-stu-id="b9800-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-389">Ordem superior 32 bits do sinalizador de recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="b9800-390">**FeaturesLow**</span><span class="sxs-lookup"><span data-stu-id="b9800-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-391">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-393">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de backup em fita win32api \| [**fita \_ obter \_ \_ parâmetros de unidade**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesLow")</span><span class="sxs-lookup"><span data-stu-id="b9800-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-394">Ordem inferior 32 bits do sinalizador de recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="b9800-395">**Id**</span><span class="sxs-lookup"><span data-stu-id="b9800-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-396">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-397">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-398">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de arquivo win32api")</span><span class="sxs-lookup"><span data-stu-id="b9800-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-399">Nome de identificação do fabricante da unidade de CD ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9800-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="b9800-400">Exemplo: "PLEXTOR CD-ROM PX-12CS 1, 1"</span><span class="sxs-lookup"><span data-stu-id="b9800-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="b9800-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b9800-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-402">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b9800-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-404">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b9800-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-405">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b9800-405">Date and time the object was installed.</span></span> <span data-ttu-id="b9800-406">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b9800-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b9800-407">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-408">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b9800-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-409">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-411">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b9800-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b9800-412">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-413">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="b9800-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-414">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-416">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="b9800-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-417">Fabricante da unidade de CD-ROM do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9800-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="b9800-418">Exemplo: "PLEXTOR"</span><span class="sxs-lookup"><span data-stu-id="b9800-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="b9800-419">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b9800-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-420">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9800-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-422">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b9800-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-423">Tamanho máximo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="b9800-424">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b9800-425">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-426">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="b9800-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-427">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9800-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-429">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="b9800-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-430">Tamanho máximo, em quilobytes, de mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="b9800-431">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b9800-432">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="b9800-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-434">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-436">Contagem máxima de partições para a unidade de fita.</span><span class="sxs-lookup"><span data-stu-id="b9800-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="b9800-437">Essa propriedade é herdada do [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-438">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="b9800-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-439">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-441">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ unidade de fita de MediaType Win32 TapeDrive \| \| ")</span><span class="sxs-lookup"><span data-stu-id="b9800-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-442">Tipo de mídia usado pelo (ou acessado por) este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="b9800-443">Nesse caso, ele é definido como "unidade de fita".</span><span class="sxs-lookup"><span data-stu-id="b9800-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="b9800-444">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b9800-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-445">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b9800-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-447">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b9800-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-448">Tamanho mínimo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="b9800-449">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b9800-450">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-451">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b9800-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-452">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-454">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b9800-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-455">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b9800-455">Label by which the object is known.</span></span> <span data-ttu-id="b9800-456">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b9800-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b9800-457">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-458">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="b9800-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-459">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b9800-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-461">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="b9800-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="b9800-462">Se a limpeza manual ou automática for possível, ela será indicada na propriedade **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b9800-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="b9800-463">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-464">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="b9800-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-465">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-467">Número máximo de mídias individuais que podem ser suportadas ou inseridas no dispositivo de acesso à mídia (quando há suporte).</span><span class="sxs-lookup"><span data-stu-id="b9800-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="b9800-468">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-469">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="b9800-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-470">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-471">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-472">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="b9800-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-473">Número de bytes inseridos entre os blocos em uma mídia de fita.</span><span class="sxs-lookup"><span data-stu-id="b9800-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="b9800-474">Essa propriedade é herdada do [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b9800-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-476">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-478">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b9800-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-479">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b9800-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b9800-480">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b9800-481">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b9800-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b9800-482">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b9800-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-483">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9800-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b9800-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-485">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b9800-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b9800-486">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="b9800-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9800-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b9800-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b9800-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="b9800-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-489">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9800-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9800-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b9800-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9800-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b9800-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-492">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b9800-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b9800-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b9800-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-494">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="b9800-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b9800-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="b9800-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-496">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b9800-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b9800-497">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="b9800-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b9800-498">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b9800-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="b9800-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-500">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="b9800-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b9800-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="b9800-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b9800-502">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="b9800-502">Timed Power-On Supported</span></span>

<span data-ttu-id="b9800-503">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="b9800-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-504">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b9800-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-505">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b9800-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-506">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9800-507">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="b9800-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b9800-508">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="b9800-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b9800-509">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-510">**ReportSetMarks**</span><span class="sxs-lookup"><span data-stu-id="b9800-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-511">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9800-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-513">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de backup em fita win32api \| [**fita \_ obter \_ \_ parâmetros de unidade**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ReportSetmarks")</span><span class="sxs-lookup"><span data-stu-id="b9800-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-514">Se for **true**, o relatório de setmark será habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9800-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="b9800-515">O relatório setmark usa um elemento registrado especializado que não contém dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9800-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="b9800-516">Esse elemento registrado é usado para fornecer um esquema de segmentação que é hierarquicamente superior a marcas de File.</span><span class="sxs-lookup"><span data-stu-id="b9800-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="b9800-517">As marcas de desmarcações fornecem um posicionamento mais rápido em fitas de alta capacidade.</span><span class="sxs-lookup"><span data-stu-id="b9800-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b9800-518"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b9800-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b9800-519">FALSE</span><span class="sxs-lookup"><span data-stu-id="b9800-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b9800-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b9800-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b9800-521">TRUE</span><span class="sxs-lookup"><span data-stu-id="b9800-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="b9800-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-523">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-525">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="b9800-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-526">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b9800-526">Current status of the object.</span></span> <span data-ttu-id="b9800-527">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="b9800-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b9800-528">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b9800-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b9800-529">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b9800-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b9800-530">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b9800-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b9800-531">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b9800-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b9800-532">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b9800-533">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b9800-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b9800-534">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b9800-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b9800-535">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b9800-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b9800-536">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b9800-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9800-537">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b9800-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b9800-538">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b9800-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b9800-539">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b9800-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b9800-540">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b9800-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b9800-541">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b9800-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b9800-542">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b9800-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b9800-543">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b9800-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b9800-544">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b9800-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b9800-545">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b9800-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b9800-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-547">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b9800-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-549">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="b9800-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b9800-550">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b9800-550">State of the logical device.</span></span> <span data-ttu-id="b9800-551">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="b9800-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b9800-552">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b9800-553">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b9800-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b9800-554">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b9800-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b9800-555">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b9800-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b9800-556">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="b9800-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b9800-557">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="b9800-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b9800-558">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b9800-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-559">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-560">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-561">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b9800-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b9800-562">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="b9800-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b9800-563">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9800-564">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b9800-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9800-565">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b9800-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9800-566">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9800-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9800-567">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b9800-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="b9800-568">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b9800-568">Name of the scoping system.</span></span>

<span data-ttu-id="b9800-569">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9800-570">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9800-570">Remarks</span></span>

<span data-ttu-id="b9800-571">A classe **Win32 \_ TapeDrive** é derivada de [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="b9800-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9800-572">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9800-572">Requirements</span></span>



| <span data-ttu-id="b9800-573">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9800-573">Requirement</span></span> | <span data-ttu-id="b9800-574">Valor</span><span class="sxs-lookup"><span data-stu-id="b9800-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9800-575">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9800-575">Minimum supported client</span></span><br/> | <span data-ttu-id="b9800-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9800-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9800-577">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9800-577">Minimum supported server</span></span><br/> | <span data-ttu-id="b9800-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9800-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9800-579">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9800-579">Namespace</span></span><br/>                | <span data-ttu-id="b9800-580">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b9800-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9800-581">MOF</span><span class="sxs-lookup"><span data-stu-id="b9800-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9800-582"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9800-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9800-583">DLL</span><span class="sxs-lookup"><span data-stu-id="b9800-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9800-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9800-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9800-585">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9800-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9800-586">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="b9800-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="b9800-587">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="b9800-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
