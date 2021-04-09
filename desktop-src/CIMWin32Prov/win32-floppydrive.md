---
description: A \_ classe WMI FloppyDrive do Win32 gerencia as funções de uma unidade de disquete.
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Classe Win32_FloppyDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089462"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="a45e3-103">\_Classe Win32 FloppyDrive</span><span class="sxs-lookup"><span data-stu-id="a45e3-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="a45e3-104">\[**Win32 \_ O FloppyDrive** não está mais disponível para uso a partir do Windows 10 e do Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="a45e3-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="a45e3-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ FloppyDrive do Win32** gerencia as funções de uma unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="a45e3-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="a45e3-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a45e3-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a45e3-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a45e3-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45e3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a45e3-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a45e3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a45e3-109">Members</span></span>

<span data-ttu-id="a45e3-110">A classe **Win32 \_ FloppyDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a45e3-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="a45e3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a45e3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a45e3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a45e3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a45e3-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a45e3-113">Methods</span></span>

<span data-ttu-id="a45e3-114">A classe **Win32 \_ FloppyDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a45e3-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="a45e3-115">Método</span><span class="sxs-lookup"><span data-stu-id="a45e3-115">Method</span></span>            | <span data-ttu-id="a45e3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a45e3-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a45e3-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a45e3-117">**Reset**</span></span>         | <span data-ttu-id="a45e3-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-118">Not implemented.</span></span> <span data-ttu-id="a45e3-119">Para obter mais informações sobre como implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="a45e3-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a45e3-120">**SetPowerState**</span></span> | <span data-ttu-id="a45e3-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-121">Not implemented.</span></span> <span data-ttu-id="a45e3-122">Para obter mais informações sobre como implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a45e3-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a45e3-123">Properties</span></span>

<span data-ttu-id="a45e3-124">A classe **Win32 \_ FloppyDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a45e3-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a45e3-125">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="a45e3-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a45e3-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a45e3-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-129">Status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-129">Status of the device.</span></span>

<span data-ttu-id="a45e3-130">Esta propriedade é herdada do [ **\_ LogicalDevice CIM**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="a45e3-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a45e3-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a45e3-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a45e3-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a45e3-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a45e3-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a45e3-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-134">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="a45e3-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a45e3-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a45e3-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a45e3-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="a45e3-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a45e3-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="a45e3-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a45e3-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="a45e3-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a45e3-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="a45e3-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a45e3-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="a45e3-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a45e3-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a45e3-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a45e3-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a45e3-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a45e3-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="a45e3-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a45e3-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="a45e3-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-145">Economia de energia-desconhecido</span><span class="sxs-lookup"><span data-stu-id="a45e3-145">Power Save - Unknown</span></span>

<span data-ttu-id="a45e3-146">O dispositivo está em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a45e3-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a45e3-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="a45e3-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-148">Economia de energia-modo de baixa energia</span><span class="sxs-lookup"><span data-stu-id="a45e3-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="a45e3-149">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a45e3-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a45e3-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-151">Economia de energia-em espera</span><span class="sxs-lookup"><span data-stu-id="a45e3-151">Power Save - Standby</span></span>

<span data-ttu-id="a45e3-152">O dispositivo não está funcionando, mas pode ser restaurado rapidamente para energia completa.</span><span class="sxs-lookup"><span data-stu-id="a45e3-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a45e3-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="a45e3-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a45e3-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a45e3-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-155">Economia de energia-aviso</span><span class="sxs-lookup"><span data-stu-id="a45e3-155">Power Save - Warning</span></span>

<span data-ttu-id="a45e3-156">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="a45e3-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a45e3-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a45e3-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-158">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="a45e3-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a45e3-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a45e3-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-160">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="a45e3-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a45e3-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a45e3-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-162">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a45e3-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="a45e3-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-164">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="a45e3-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-165">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="a45e3-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-166">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a45e3-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-168">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="a45e3-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-169">Matriz de recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="a45e3-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="a45e3-170">Por exemplo, o dispositivo pode dar suporte a acesso aleatório, mídia removível e limpeza automática.</span><span class="sxs-lookup"><span data-stu-id="a45e3-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="a45e3-171">Nesse caso, os valores 3, 7 e 9 seriam gravados na matriz.</span><span class="sxs-lookup"><span data-stu-id="a45e3-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="a45e3-172">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a45e3-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a45e3-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a45e3-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a45e3-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="a45e3-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="a45e3-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="a45e3-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="a45e3-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="a45e3-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="a45e3-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="a45e3-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="a45e3-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="a45e3-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="a45e3-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="a45e3-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="a45e3-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-181">Dá suporte a mídia removível</span><span class="sxs-lookup"><span data-stu-id="a45e3-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="a45e3-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="a45e3-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="a45e3-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="a45e3-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="a45e3-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="a45e3-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="a45e3-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="a45e3-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-186">Dá suporte à mídia Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="a45e3-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="a45e3-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="a45e3-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-188">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a45e3-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-189">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-191">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="a45e3-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-192">Matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do controlador serial indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="a45e3-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="a45e3-193">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="a45e3-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="a45e3-194">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-195">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a45e3-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-198">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a45e3-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-199">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a45e3-199">Short description of the object.</span></span>

<span data-ttu-id="a45e3-200">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-201">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="a45e3-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-204">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada pelo dispositivo para dar suporte à compactação.</span><span class="sxs-lookup"><span data-stu-id="a45e3-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="a45e3-205">Se não for possível ou não desejar descrever o esquema de compactação (talvez porque não seja conhecido), use "desconhecido" para representar que não é conhecido se o dispositivo dá suporte a recursos de compactação ou não; "Compactado" para representar que o dispositivo dá suporte a recursos de compactação, mas o esquema de compactação não é conhecido ou não é divulgado; e "não compactado" para representar que o dispositivo não oferece suporte a recursos de compactação.</span><span class="sxs-lookup"><span data-stu-id="a45e3-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="a45e3-206">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="a45e3-207">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a45e3-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-208">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="a45e3-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="a45e3-209">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="a45e3-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-210">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="a45e3-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="a45e3-211">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="a45e3-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-212">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="a45e3-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a45e3-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-214">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a45e3-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-216">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a45e3-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-217">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a45e3-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="a45e3-218">Esta propriedade é herdada do [ **\_ LogicalDevice CIM**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="a45e3-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a45e3-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a45e3-220"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="a45e3-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-221">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a45e3-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a45e3-223">(1)</span><span class="sxs-lookup"><span data-stu-id="a45e3-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-224">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a45e3-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a45e3-226">(2)</span><span class="sxs-lookup"><span data-stu-id="a45e3-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a45e3-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a45e3-228">(3)</span><span class="sxs-lookup"><span data-stu-id="a45e3-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-229">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="a45e3-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a45e3-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a45e3-231">(4)</span><span class="sxs-lookup"><span data-stu-id="a45e3-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-232">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-232">Device is not working properly.</span></span> <span data-ttu-id="a45e3-233">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a45e3-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a45e3-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a45e3-235">(5)</span><span class="sxs-lookup"><span data-stu-id="a45e3-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-236">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="a45e3-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a45e3-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a45e3-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="a45e3-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-239">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a45e3-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a45e3-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a45e3-241">(7)</span><span class="sxs-lookup"><span data-stu-id="a45e3-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a45e3-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a45e3-243">(8)</span><span class="sxs-lookup"><span data-stu-id="a45e3-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-244">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a45e3-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a45e3-246">(9)</span><span class="sxs-lookup"><span data-stu-id="a45e3-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-247">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-247">Device is not working properly.</span></span> <span data-ttu-id="a45e3-248">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a45e3-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a45e3-250">(10)</span><span class="sxs-lookup"><span data-stu-id="a45e3-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-251">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a45e3-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a45e3-253">(11)</span><span class="sxs-lookup"><span data-stu-id="a45e3-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-254">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a45e3-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a45e3-256">12</span><span class="sxs-lookup"><span data-stu-id="a45e3-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-257">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="a45e3-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a45e3-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a45e3-259">(13)</span><span class="sxs-lookup"><span data-stu-id="a45e3-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-260">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a45e3-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a45e3-262">(14)</span><span class="sxs-lookup"><span data-stu-id="a45e3-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-263">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a45e3-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a45e3-265">(15)</span><span class="sxs-lookup"><span data-stu-id="a45e3-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-266">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="a45e3-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a45e3-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a45e3-268">(16)</span><span class="sxs-lookup"><span data-stu-id="a45e3-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-269">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="a45e3-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a45e3-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a45e3-271">(17)</span><span class="sxs-lookup"><span data-stu-id="a45e3-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-272">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a45e3-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a45e3-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a45e3-274">(18)</span><span class="sxs-lookup"><span data-stu-id="a45e3-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-275">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="a45e3-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a45e3-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a45e3-277">(19)</span><span class="sxs-lookup"><span data-stu-id="a45e3-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a45e3-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a45e3-279">(20)</span><span class="sxs-lookup"><span data-stu-id="a45e3-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-280">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a45e3-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a45e3-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a45e3-282">(21)</span><span class="sxs-lookup"><span data-stu-id="a45e3-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-283">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a45e3-283">System failure.</span></span> <span data-ttu-id="a45e3-284">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a45e3-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a45e3-285">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a45e3-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a45e3-287">(22)</span><span class="sxs-lookup"><span data-stu-id="a45e3-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-288">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a45e3-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a45e3-290">(23)</span><span class="sxs-lookup"><span data-stu-id="a45e3-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-291">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a45e3-291">System failure.</span></span> <span data-ttu-id="a45e3-292">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a45e3-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a45e3-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a45e3-294">(24)</span><span class="sxs-lookup"><span data-stu-id="a45e3-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-295">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="a45e3-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a45e3-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a45e3-297">(25)</span><span class="sxs-lookup"><span data-stu-id="a45e3-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-298">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a45e3-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a45e3-300">(26)</span><span class="sxs-lookup"><span data-stu-id="a45e3-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-301">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a45e3-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a45e3-303">(27)</span><span class="sxs-lookup"><span data-stu-id="a45e3-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-304">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="a45e3-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a45e3-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a45e3-306">(28)</span><span class="sxs-lookup"><span data-stu-id="a45e3-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-307">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="a45e3-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a45e3-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a45e3-309">(29)</span><span class="sxs-lookup"><span data-stu-id="a45e3-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-310">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-310">Device is disabled.</span></span> <span data-ttu-id="a45e3-311">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="a45e3-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a45e3-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a45e3-313">(30)</span><span class="sxs-lookup"><span data-stu-id="a45e3-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-314">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a45e3-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a45e3-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a45e3-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a45e3-316">(31)</span><span class="sxs-lookup"><span data-stu-id="a45e3-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-317">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-317">Device is not working properly.</span></span> <span data-ttu-id="a45e3-318">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="a45e3-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a45e3-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-320">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a45e3-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-322">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a45e3-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-323">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a45e3-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a45e3-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-325">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a45e3-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-328">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a45e3-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-329">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a45e3-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a45e3-330">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a45e3-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a45e3-331">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-332">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="a45e3-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-333">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a45e3-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-335">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a45e3-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-336">Tamanho de bloco padrão, em bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="a45e3-337">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a45e3-338">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a45e3-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-339">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a45e3-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-342">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a45e3-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-343">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a45e3-343">Description of the object.</span></span>

<span data-ttu-id="a45e3-344">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a45e3-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-348">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a45e3-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-349">Identificador exclusivo da unidade de disquete com outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="a45e3-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="a45e3-350">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a45e3-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-352">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a45e3-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-354">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a45e3-355">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a45e3-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-357">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-359">Cadeia de caracteres de forma livre que fornece mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="a45e3-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="a45e3-360">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-361">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="a45e3-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-362">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-364">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="a45e3-365">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a45e3-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-367">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a45e3-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-369">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a45e3-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-370">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-370">Date and time the object was installed.</span></span> <span data-ttu-id="a45e3-371">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a45e3-372">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-373">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a45e3-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-374">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a45e3-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-376">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a45e3-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a45e3-377">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-378">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="a45e3-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-381">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="a45e3-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-382">Nome do fabricante da unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="a45e3-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="a45e3-383">Exemplo: "Acme"</span><span class="sxs-lookup"><span data-stu-id="a45e3-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-384">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="a45e3-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-385">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a45e3-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-387">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a45e3-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-388">Tamanho máximo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="a45e3-389">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a45e3-390">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a45e3-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-391">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="a45e3-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-392">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a45e3-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="a45e3-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-395">Tamanho máximo, em quilobytes, de mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="a45e3-396">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a45e3-397">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a45e3-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-398">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="a45e3-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-399">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a45e3-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-401">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="a45e3-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-402">Tamanho mínimo do bloco, em bytes, para a mídia acessada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="a45e3-403">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="a45e3-404">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a45e3-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-405">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a45e3-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-408">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a45e3-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-409">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="a45e3-409">Label by which the object is known.</span></span> <span data-ttu-id="a45e3-410">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="a45e3-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a45e3-411">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-412">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="a45e3-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-413">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a45e3-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-415">Se **for true**, o dispositivo de acesso à mídia exigirá limpeza.</span><span class="sxs-lookup"><span data-stu-id="a45e3-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="a45e3-416">Se a limpeza manual ou automática for possível, ela será indicada na propriedade **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="a45e3-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="a45e3-417">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-418">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="a45e3-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-419">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a45e3-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-421">Número máximo de mídias individuais que podem ser suportadas ou inseridas no dispositivo de acesso à mídia (quando há suporte).</span><span class="sxs-lookup"><span data-stu-id="a45e3-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="a45e3-422">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a45e3-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-426">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a45e3-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-427">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a45e3-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a45e3-428">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a45e3-429">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a45e3-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a45e3-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-431">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a45e3-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-433">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a45e3-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a45e3-434">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="a45e3-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a45e3-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a45e3-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a45e3-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="a45e3-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a45e3-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a45e3-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a45e3-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a45e3-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-439">habilitado</span><span class="sxs-lookup"><span data-stu-id="a45e3-439">Enabled</span></span>

<span data-ttu-id="a45e3-440">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a45e3-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a45e3-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a45e3-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-442">Modos de economia de energia inseridos automaticamente</span><span class="sxs-lookup"><span data-stu-id="a45e3-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="a45e3-443">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="a45e3-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a45e3-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="a45e3-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-445">Estado de energia configurável</span><span class="sxs-lookup"><span data-stu-id="a45e3-445">Power State Settable</span></span>

<span data-ttu-id="a45e3-446">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="a45e3-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a45e3-447">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a45e3-448">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a45e3-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a45e3-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="a45e3-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-450">Ciclo de energia com suporte</span><span class="sxs-lookup"><span data-stu-id="a45e3-450">Power Cycling Supported</span></span>

<span data-ttu-id="a45e3-451">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="a45e3-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a45e3-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="a45e3-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a45e3-453">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="a45e3-453">Timed Power-On Supported</span></span>

<span data-ttu-id="a45e3-454">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="a45e3-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-455">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a45e3-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-456">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a45e3-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-458">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="a45e3-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="a45e3-459">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="a45e3-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a45e3-460">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-461">**Status**</span><span class="sxs-lookup"><span data-stu-id="a45e3-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-462">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-464">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a45e3-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-465">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a45e3-465">Current status of the object.</span></span> <span data-ttu-id="a45e3-466">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a45e3-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a45e3-467">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a45e3-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="a45e3-468">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="a45e3-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a45e3-469">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a45e3-470">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="a45e3-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a45e3-471">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a45e3-472">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="a45e3-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a45e3-473">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a45e3-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a45e3-474">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a45e3-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a45e3-475">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a45e3-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a45e3-476">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a45e3-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a45e3-477">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a45e3-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a45e3-478">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a45e3-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a45e3-479">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a45e3-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a45e3-480">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a45e3-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a45e3-481">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a45e3-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a45e3-482">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a45e3-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a45e3-483">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a45e3-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a45e3-484">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a45e3-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a45e3-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-486">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a45e3-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-488">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="a45e3-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-489">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a45e3-489">State of the logical device.</span></span> <span data-ttu-id="a45e3-490">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="a45e3-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="a45e3-491">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a45e3-492">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a45e3-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a45e3-493">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a45e3-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a45e3-494">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a45e3-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a45e3-495">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a45e3-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a45e3-496">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="a45e3-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a45e3-497">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a45e3-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-498">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-500">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a45e3-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-501">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="a45e3-502">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a45e3-503">Esta propriedade é herdada do [ **\_ LogicalDevice CIM**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="a45e3-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="a45e3-504">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a45e3-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a45e3-505">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a45e3-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-506">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a45e3-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a45e3-507">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a45e3-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a45e3-508">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a45e3-508">Name of the scoping system.</span></span>

<span data-ttu-id="a45e3-509">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a45e3-510">Comentários</span><span class="sxs-lookup"><span data-stu-id="a45e3-510">Remarks</span></span>

<span data-ttu-id="a45e3-511">A classe **Win32 \_ FloppyDrive** é derivada de [**\_ DisketteDrive CIM**](cim-diskettedrive.md) que deriva do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="a45e3-512">A classe **CIM \_ MediaAccessDevice** deriva do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a45e3-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a45e3-513">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a45e3-513">Requirements</span></span>



| <span data-ttu-id="a45e3-514">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45e3-514">Requirement</span></span> | <span data-ttu-id="a45e3-515">Valor</span><span class="sxs-lookup"><span data-stu-id="a45e3-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a45e3-516">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a45e3-516">Minimum supported client</span></span><br/> | <span data-ttu-id="a45e3-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a45e3-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a45e3-518">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a45e3-518">Minimum supported server</span></span><br/> | <span data-ttu-id="a45e3-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a45e3-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a45e3-520">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a45e3-520">End of client support</span></span><br/>    | <span data-ttu-id="a45e3-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a45e3-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="a45e3-522">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a45e3-522">End of server support</span></span><br/>    | <span data-ttu-id="a45e3-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a45e3-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="a45e3-524">Namespace</span><span class="sxs-lookup"><span data-stu-id="a45e3-524">Namespace</span></span><br/>                | <span data-ttu-id="a45e3-525">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a45e3-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a45e3-526">MOF</span><span class="sxs-lookup"><span data-stu-id="a45e3-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a45e3-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a45e3-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a45e3-528">DLL</span><span class="sxs-lookup"><span data-stu-id="a45e3-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a45e3-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a45e3-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45e3-530">Confira também</span><span class="sxs-lookup"><span data-stu-id="a45e3-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45e3-531">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="a45e3-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="a45e3-532">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="a45e3-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

