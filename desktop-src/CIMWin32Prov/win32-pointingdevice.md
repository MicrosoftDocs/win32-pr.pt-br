---
description: A \_ classe WMI PointingDevice do Win32 representa um dispositivo de entrada usado para apontar e selecionar regiões na exibição de um sistema de computador executando o Windows.
ms.assetid: ed81abe3-3d8f-48aa-ab64-9e6c87e44f64
ms.tgt_platform: multiple
title: Classe Win32_PointingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PointingDevice
- Win32_PointingDevice.Reset
- Win32_PointingDevice.SetPowerState
- Win32_PointingDevice.Availability
- Win32_PointingDevice.Caption
- Win32_PointingDevice.ConfigManagerErrorCode
- Win32_PointingDevice.ConfigManagerUserConfig
- Win32_PointingDevice.CreationClassName
- Win32_PointingDevice.Description
- Win32_PointingDevice.DeviceID
- Win32_PointingDevice.DeviceInterface
- Win32_PointingDevice.DoubleSpeedThreshold
- Win32_PointingDevice.ErrorCleared
- Win32_PointingDevice.ErrorDescription
- Win32_PointingDevice.Handedness
- Win32_PointingDevice.HardwareType
- Win32_PointingDevice.InfFileName
- Win32_PointingDevice.InfSection
- Win32_PointingDevice.InstallDate
- Win32_PointingDevice.IsLocked
- Win32_PointingDevice.LastErrorCode
- Win32_PointingDevice.Manufacturer
- Win32_PointingDevice.Name
- Win32_PointingDevice.NumberOfButtons
- Win32_PointingDevice.PNPDeviceID
- Win32_PointingDevice.PointingType
- Win32_PointingDevice.PowerManagementCapabilities
- Win32_PointingDevice.PowerManagementSupported
- Win32_PointingDevice.QuadSpeedThreshold
- Win32_PointingDevice.Resolution
- Win32_PointingDevice.SampleRate
- Win32_PointingDevice.Status
- Win32_PointingDevice.StatusInfo
- Win32_PointingDevice.Synch
- Win32_PointingDevice.SystemCreationClassName
- Win32_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e4f2359e19476dfae111fc361f48e6f73d8cfac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762759"
---
# <a name="win32_pointingdevice-class"></a><span data-ttu-id="81bf6-103">\_Classe Win32 PointingDevice</span><span class="sxs-lookup"><span data-stu-id="81bf6-103">Win32\_PointingDevice class</span></span>

<span data-ttu-id="81bf6-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PointingDevice do Win32** representa um dispositivo de entrada usado para apontar e selecionar regiões na exibição de um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="81bf6-104">The **Win32\_PointingDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents an input device used to point to and select regions on the display of a computer system running Windows.</span></span> <span data-ttu-id="81bf6-105">Qualquer dispositivo usado para manipular um ponteiro ou apontar para a exibição em um sistema de computador que executa o Windows é membro dessa classe.</span><span class="sxs-lookup"><span data-stu-id="81bf6-105">Any device used to manipulate a pointer, or point to the display on a computer system running Windows is a member of this class.</span></span>

<span data-ttu-id="81bf6-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="81bf6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="81bf6-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="81bf6-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bf6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81bf6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PointingDevice : CIM_PointingDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DeviceInterface;
  uint32   DoubleSpeedThreshold;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  string   HardwareType;
  string   InfFileName;
  string   InfSection;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   QuadSpeedThreshold;
  uint32   Resolution;
  uint32   SampleRate;
  string   Status;
  uint16   StatusInfo;
  uint32   Synch;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="81bf6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="81bf6-109">Members</span></span>

<span data-ttu-id="81bf6-110">A classe **Win32 \_ PointingDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="81bf6-110">The **Win32\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="81bf6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="81bf6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="81bf6-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81bf6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="81bf6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="81bf6-113">Methods</span></span>

<span data-ttu-id="81bf6-114">A classe **Win32 \_ PointingDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="81bf6-114">The **Win32\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="81bf6-115">Método</span><span class="sxs-lookup"><span data-stu-id="81bf6-115">Method</span></span>            | <span data-ttu-id="81bf6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="81bf6-116">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81bf6-117">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="81bf6-117">**Reset**</span></span>         | <span data-ttu-id="81bf6-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-118">Not implemented.</span></span> <span data-ttu-id="81bf6-119">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/>                 |
| <span data-ttu-id="81bf6-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="81bf6-120">**SetPowerState**</span></span> | <span data-ttu-id="81bf6-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-121">Not implemented.</span></span> <span data-ttu-id="81bf6-122">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="81bf6-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81bf6-123">Properties</span></span>

<span data-ttu-id="81bf6-124">A classe **Win32 \_ PointingDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="81bf6-124">The **Win32\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81bf6-125">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="81bf6-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bf6-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-128">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="81bf6-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-129">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-129">Availability and status of the device.</span></span>

<span data-ttu-id="81bf6-130">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81bf6-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="81bf6-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-134">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="81bf6-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="81bf6-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="81bf6-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="81bf6-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="81bf6-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81bf6-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="81bf6-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="81bf6-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="81bf6-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="81bf6-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="81bf6-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="81bf6-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="81bf6-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81bf6-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="81bf6-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="81bf6-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="81bf6-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="81bf6-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="81bf6-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="81bf6-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="81bf6-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="81bf6-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="81bf6-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="81bf6-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="81bf6-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="81bf6-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="81bf6-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="81bf6-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="81bf6-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="81bf6-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="81bf6-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="81bf6-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="81bf6-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="81bf6-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="81bf6-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="81bf6-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="81bf6-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="81bf6-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="81bf6-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="81bf6-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="81bf6-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="81bf6-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-161">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="81bf6-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-164">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="81bf6-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-165">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="81bf6-165">Short description of the object.</span></span>

<span data-ttu-id="81bf6-166">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81bf6-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-168">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-170">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81bf6-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-171">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="81bf6-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="81bf6-172">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="81bf6-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="81bf6-174"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="81bf6-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-175">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="81bf6-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="81bf6-177">(1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-178">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81bf6-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="81bf6-180">(2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="81bf6-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="81bf6-182">(3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-183">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="81bf6-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="81bf6-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="81bf6-185">(4)</span><span class="sxs-lookup"><span data-stu-id="81bf6-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-186">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-186">Device is not working properly.</span></span> <span data-ttu-id="81bf6-187">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="81bf6-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="81bf6-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="81bf6-189">(5)</span><span class="sxs-lookup"><span data-stu-id="81bf6-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-190">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="81bf6-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="81bf6-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="81bf6-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="81bf6-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-193">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="81bf6-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="81bf6-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="81bf6-195">(7)</span><span class="sxs-lookup"><span data-stu-id="81bf6-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="81bf6-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="81bf6-197">(8)</span><span class="sxs-lookup"><span data-stu-id="81bf6-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-198">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="81bf6-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="81bf6-200">(9)</span><span class="sxs-lookup"><span data-stu-id="81bf6-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-201">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-201">Device is not working properly.</span></span> <span data-ttu-id="81bf6-202">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="81bf6-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="81bf6-204">(10)</span><span class="sxs-lookup"><span data-stu-id="81bf6-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-205">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="81bf6-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="81bf6-207">(11)</span><span class="sxs-lookup"><span data-stu-id="81bf6-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-208">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="81bf6-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="81bf6-210">12</span><span class="sxs-lookup"><span data-stu-id="81bf6-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-211">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="81bf6-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="81bf6-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="81bf6-213">(13)</span><span class="sxs-lookup"><span data-stu-id="81bf6-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-214">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="81bf6-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="81bf6-216">(14)</span><span class="sxs-lookup"><span data-stu-id="81bf6-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-217">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="81bf6-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="81bf6-219">(15)</span><span class="sxs-lookup"><span data-stu-id="81bf6-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-220">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="81bf6-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="81bf6-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="81bf6-222">(16)</span><span class="sxs-lookup"><span data-stu-id="81bf6-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-223">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="81bf6-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="81bf6-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="81bf6-225">(17)</span><span class="sxs-lookup"><span data-stu-id="81bf6-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-226">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="81bf6-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81bf6-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="81bf6-228">(18)</span><span class="sxs-lookup"><span data-stu-id="81bf6-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-229">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="81bf6-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="81bf6-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="81bf6-231">(19)</span><span class="sxs-lookup"><span data-stu-id="81bf6-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="81bf6-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="81bf6-233">(20)</span><span class="sxs-lookup"><span data-stu-id="81bf6-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-234">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="81bf6-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="81bf6-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="81bf6-236">(21)</span><span class="sxs-lookup"><span data-stu-id="81bf6-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-237">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="81bf6-237">System failure.</span></span> <span data-ttu-id="81bf6-238">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="81bf6-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="81bf6-239">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="81bf6-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="81bf6-241">(22)</span><span class="sxs-lookup"><span data-stu-id="81bf6-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-242">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="81bf6-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="81bf6-244">(23)</span><span class="sxs-lookup"><span data-stu-id="81bf6-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-245">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="81bf6-245">System failure.</span></span> <span data-ttu-id="81bf6-246">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="81bf6-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="81bf6-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="81bf6-248">(24)</span><span class="sxs-lookup"><span data-stu-id="81bf6-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-249">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="81bf6-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="81bf6-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="81bf6-251">(25)</span><span class="sxs-lookup"><span data-stu-id="81bf6-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-252">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="81bf6-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="81bf6-254">(26)</span><span class="sxs-lookup"><span data-stu-id="81bf6-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-255">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="81bf6-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="81bf6-257">(27)</span><span class="sxs-lookup"><span data-stu-id="81bf6-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-258">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="81bf6-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="81bf6-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="81bf6-260">(28)</span><span class="sxs-lookup"><span data-stu-id="81bf6-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-261">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="81bf6-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="81bf6-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="81bf6-263">(29)</span><span class="sxs-lookup"><span data-stu-id="81bf6-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-264">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-264">Device is disabled.</span></span> <span data-ttu-id="81bf6-265">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="81bf6-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="81bf6-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="81bf6-267">(30)</span><span class="sxs-lookup"><span data-stu-id="81bf6-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-268">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="81bf6-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="81bf6-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="81bf6-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="81bf6-270">(31)</span><span class="sxs-lookup"><span data-stu-id="81bf6-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-271">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-271">Device is not working properly.</span></span> <span data-ttu-id="81bf6-272">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="81bf6-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="81bf6-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-274">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81bf6-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-276">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81bf6-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-277">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="81bf6-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="81bf6-278">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81bf6-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-282">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="81bf6-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-283">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="81bf6-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="81bf6-284">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="81bf6-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="81bf6-285">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-286">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="81bf6-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-289">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="81bf6-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-290">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="81bf6-290">Description of the object.</span></span>

<span data-ttu-id="81bf6-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="81bf6-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-295">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="81bf6-295">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-296">Identificador exclusivo do dispositivo apontador com outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="81bf6-296">Unique identifier of the pointing device with other devices on the system.</span></span>

<span data-ttu-id="81bf6-297">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-298">**DeviceInterface**</span><span class="sxs-lookup"><span data-stu-id="81bf6-298">**DeviceInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-299">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bf6-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-301">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| interface SMBIOS tipo 21 \| ")</span><span class="sxs-lookup"><span data-stu-id="81bf6-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 21\|Interface")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-302">Tipo de interface usada para o dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="81bf6-302">Type of interface used for the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81bf6-303">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-303">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-304">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-304">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial"></span><span id="serial"></span><span id="SERIAL"></span>

<span data-ttu-id="81bf6-305">**Serial** (3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-305">**Serial** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="81bf6-306">**PS/2** (4)</span><span class="sxs-lookup"><span data-stu-id="81bf6-306">**PS/2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="81bf6-307">**Infravermelho** (5)</span><span class="sxs-lookup"><span data-stu-id="81bf6-307">**Infrared** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="81bf6-308">**HP-Hil** (6)</span><span class="sxs-lookup"><span data-stu-id="81bf6-308">**HP-HIL** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="81bf6-309">**Mouse de barramento** (7)</span><span class="sxs-lookup"><span data-stu-id="81bf6-309">**Bus mouse** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB__Apple_Desktop_Bus_"></span><span id="adb__apple_desktop_bus_"></span><span id="ADB__APPLE_DESKTOP_BUS_"></span>

<span data-ttu-id="81bf6-310">**ADB (barramento de área de trabalho da Apple)** (8)</span><span class="sxs-lookup"><span data-stu-id="81bf6-310">**ADB (Apple Desktop Bus)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_DB-9"></span><span id="bus_mouse_db-9"></span><span id="BUS_MOUSE_DB-9"></span>

<span data-ttu-id="81bf6-311">**Banco de mouse do barramento-9** (160)</span><span class="sxs-lookup"><span data-stu-id="81bf6-311">**Bus mouse DB-9** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_micro-DIN"></span><span id="bus_mouse_micro-din"></span><span id="BUS_MOUSE_MICRO-DIN"></span>

<span data-ttu-id="81bf6-312">**Micro-DIN do mouse do barramento** (161)</span><span class="sxs-lookup"><span data-stu-id="81bf6-312">**Bus mouse micro-DIN** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="81bf6-313">**USB** (162)</span><span class="sxs-lookup"><span data-stu-id="81bf6-313">**USB** (162)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-314">**DoubleSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="81bf6-314">**DoubleSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-315">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-317">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| funções de informações do sistema \| SystemParametersInfo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="81bf6-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-318">Um dos dois valores de aceleração.</span><span class="sxs-lookup"><span data-stu-id="81bf6-318">One of two acceleration values.</span></span> <span data-ttu-id="81bf6-319">A sensibilidade do dispositivo apontador dobra (alterna do primeiro para o segundo valor) quando o dispositivo apontador move uma distância maior do que esse valor de limite.</span><span class="sxs-lookup"><span data-stu-id="81bf6-319">The sensitivity of the pointing device doubles (toggles from the first to the second value) when the pointing device moves a distance greater than this threshold value.</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="81bf6-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-321">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81bf6-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-323">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-323">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="81bf6-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="81bf6-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-328">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="81bf6-328">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="81bf6-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-330">**Direção**</span><span class="sxs-lookup"><span data-stu-id="81bf6-330">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-331">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bf6-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-333">Configuração do dispositivo apontador para operação esquerda ou direita.</span><span class="sxs-lookup"><span data-stu-id="81bf6-333">Configuration of the pointing device for left-hand or right-hand operation.</span></span>

<span data-ttu-id="81bf6-334">Essa propriedade é herdada do [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-334">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="81bf6-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81bf6-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="81bf6-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Operação da mão direita** (2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-338">Right-Handed operação</span><span class="sxs-lookup"><span data-stu-id="81bf6-338">Right-Handed Operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="81bf6-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Operação da mão esquerda** (3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-340">Left-Handed operação</span><span class="sxs-lookup"><span data-stu-id="81bf6-340">Left-Handed Operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-341">**HardwareType**</span><span class="sxs-lookup"><span data-stu-id="81bf6-341">**HardwareType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-344">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System o \\ \\ \\ \\ controle ControlSet001 \\ \\ classe \| DriverDesc")</span><span class="sxs-lookup"><span data-stu-id="81bf6-344">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\ControlSet001\\\\Control\\\\Class\|DriverDesc")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-345">Tipo de hardware usado para o dispositivo apontador do Windows.</span><span class="sxs-lookup"><span data-stu-id="81bf6-345">Type of hardware used for the Windows pointing device.</span></span>

<span data-ttu-id="81bf6-346">Exemplo: "MICROSOFT PS2 MOUSE"</span><span class="sxs-lookup"><span data-stu-id="81bf6-346">Example: "MICROSOFT PS2 MOUSE"</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-347">**InfFileName**</span><span class="sxs-lookup"><span data-stu-id="81bf6-347">**InfFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-348">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-350">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="81bf6-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-351">Nome do arquivo. inf para o dispositivo apontador do Windows.</span><span class="sxs-lookup"><span data-stu-id="81bf6-351">Name of the .inf file for the Windows pointing device.</span></span>

<span data-ttu-id="81bf6-352">Exemplo: "AB. inf"</span><span class="sxs-lookup"><span data-stu-id="81bf6-352">Example: "ab.inf"</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-353">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="81bf6-353">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-354">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-356">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="81bf6-356">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-357">Seção do arquivo. inf que contém informações de configuração para o dispositivo apontador do Windows.</span><span class="sxs-lookup"><span data-stu-id="81bf6-357">Section of the .inf file that holds configuration information for the Windows pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-358">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="81bf6-358">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-359">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="81bf6-359">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-361">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="81bf6-361">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-362">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-362">Date and time the object was installed.</span></span> <span data-ttu-id="81bf6-363">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-363">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="81bf6-364">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-365">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="81bf6-365">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-366">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81bf6-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-368">Se for **true**, o dispositivo será bloqueado, impedindo a entrada ou saída do usuário.</span><span class="sxs-lookup"><span data-stu-id="81bf6-368">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="81bf6-369">Essa propriedade é herdada [**do \_ userdevice do CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-369">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="81bf6-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-371">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-373">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bf6-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="81bf6-374">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-375">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="81bf6-375">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-378">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="81bf6-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-379">Nome do fabricante do processador.</span><span class="sxs-lookup"><span data-stu-id="81bf6-379">Name of the processor's manufacturer.</span></span>

<span data-ttu-id="81bf6-380">Exemplo: "GenuineSilicon"</span><span class="sxs-lookup"><span data-stu-id="81bf6-380">Example: "GenuineSilicon"</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-381">**Nome**</span><span class="sxs-lookup"><span data-stu-id="81bf6-381">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-384">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="81bf6-384">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-385">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="81bf6-385">Label by which the object is known.</span></span> <span data-ttu-id="81bf6-386">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="81bf6-386">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="81bf6-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-388">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="81bf6-388">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-389">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="81bf6-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-391">Número de botões no dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="81bf6-391">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="81bf6-392">Essa propriedade é herdada do [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-392">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="81bf6-393">Exemplo: 2</span><span class="sxs-lookup"><span data-stu-id="81bf6-393">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-394">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="81bf6-394">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-395">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-397">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="81bf6-397">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-398">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bf6-398">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="81bf6-399">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="81bf6-400">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="81bf6-400">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-401">**Ponto de apontar**</span><span class="sxs-lookup"><span data-stu-id="81bf6-401">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-402">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bf6-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-404">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo apontador DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="81bf6-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-405">Tipo de dispositivo apontador.</span><span class="sxs-lookup"><span data-stu-id="81bf6-405">Type of pointing device.</span></span>

<span data-ttu-id="81bf6-406">Essa propriedade é herdada do [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-406">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81bf6-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="81bf6-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="81bf6-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Rastrear bola** (4)</span><span class="sxs-lookup"><span data-stu-id="81bf6-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-411">Ficar</span><span class="sxs-lookup"><span data-stu-id="81bf6-411">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="81bf6-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Ponto de controle** (5)</span><span class="sxs-lookup"><span data-stu-id="81bf6-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="81bf6-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Ponto de deslizamento** (6)</span><span class="sxs-lookup"><span data-stu-id="81bf6-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="81bf6-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch pad** (7)</span><span class="sxs-lookup"><span data-stu-id="81bf6-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="81bf6-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Tela sensível ao toque** (8)</span><span class="sxs-lookup"><span data-stu-id="81bf6-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="81bf6-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Sensor de mouse-óptico** (9)</span><span class="sxs-lookup"><span data-stu-id="81bf6-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-417">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="81bf6-417">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-418">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bf6-418">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-420">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bf6-420">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="81bf6-421">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="81bf6-421">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="81bf6-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="81bf6-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="81bf6-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="81bf6-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-426">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="81bf6-426">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="81bf6-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="81bf6-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-428">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="81bf6-428">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="81bf6-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="81bf6-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-430">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="81bf6-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="81bf6-431">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-431">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="81bf6-432">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-432">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="81bf6-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="81bf6-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-434">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="81bf6-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="81bf6-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="81bf6-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="81bf6-436">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="81bf6-436">Timed Power-On Supported</span></span>

<span data-ttu-id="81bf6-437">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="81bf6-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-438">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="81bf6-438">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-439">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="81bf6-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-441">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="81bf6-441">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="81bf6-442">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="81bf6-442">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="81bf6-443">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-444">**QuadSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="81bf6-444">**QuadSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-445">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-447">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| funções de informações do sistema \| SystemParametersInfo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="81bf6-447">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-448">Um dos dois valores de limite de aceleração.</span><span class="sxs-lookup"><span data-stu-id="81bf6-448">One of two acceleration threshold values.</span></span> <span data-ttu-id="81bf6-449">O sistema dobra a velocidade do movimento do ponteiro quando o dispositivo do ponteiro move uma distância maior que esse valor.</span><span class="sxs-lookup"><span data-stu-id="81bf6-449">The system doubles the speed of the pointer movement when the pointer device moves a distance greater than this value.</span></span> <span data-ttu-id="81bf6-450">Como esse aumento de velocidade ocorre depois que o valor de **DoubleSpeedThreshold** foi atingido, o ponteiro se move efetivamente em quatro vezes sua velocidade original.</span><span class="sxs-lookup"><span data-stu-id="81bf6-450">Because this speed increase occurs after the **DoubleSpeedThreshold** value has been met, the pointer effectively moves at four times its original speed.</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-451">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="81bf6-451">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-452">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-454">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("contagens por polegada")</span><span class="sxs-lookup"><span data-stu-id="81bf6-454">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-455">Resolução de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="81bf6-455">Tracking resolution.</span></span>

<span data-ttu-id="81bf6-456">Essa propriedade é herdada do [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-456">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="81bf6-457">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="81bf6-457">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-458">**SampleRate**</span><span class="sxs-lookup"><span data-stu-id="81bf6-458">**SampleRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-459">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-459">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-461">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| amostra"), [**unidades**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="81bf6-461">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-462">Taxa na qual o dispositivo apontador é sondado quanto a informações de entrada.</span><span class="sxs-lookup"><span data-stu-id="81bf6-462">Rate at which the pointing device is polled for input information.</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-463">**Status**</span><span class="sxs-lookup"><span data-stu-id="81bf6-463">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-464">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-466">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="81bf6-466">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-467">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="81bf6-467">Current status of the object.</span></span> <span data-ttu-id="81bf6-468">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="81bf6-468">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="81bf6-469">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="81bf6-469">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="81bf6-470">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="81bf6-470">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="81bf6-471">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-471">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="81bf6-472">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="81bf6-472">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="81bf6-473">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-473">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="81bf6-474">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="81bf6-474">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="81bf6-475">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="81bf6-475">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="81bf6-476">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="81bf6-476">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="81bf6-477">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="81bf6-477">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-478">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="81bf6-478">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="81bf6-479">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="81bf6-479">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="81bf6-480">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="81bf6-480">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="81bf6-481">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="81bf6-481">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="81bf6-482">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="81bf6-482">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="81bf6-483">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="81bf6-483">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="81bf6-484">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="81bf6-484">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="81bf6-485">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="81bf6-485">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="81bf6-486">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="81bf6-486">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-487">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="81bf6-487">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-488">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="81bf6-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-490">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="81bf6-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-491">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="81bf6-491">State of the logical device.</span></span> <span data-ttu-id="81bf6-492">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="81bf6-492">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="81bf6-493">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-493">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="81bf6-494">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="81bf6-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="81bf6-495">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="81bf6-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="81bf6-496">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="81bf6-496">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="81bf6-497">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="81bf6-497">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="81bf6-498">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="81bf6-498">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="81bf6-499">**Sincronização**</span><span class="sxs-lookup"><span data-stu-id="81bf6-499">**Synch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-500">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81bf6-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-501">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-502">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| MouseSynchIn100ns"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")</span><span class="sxs-lookup"><span data-stu-id="81bf6-502">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|MouseSynchIn100ns"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-503">Período de tempo após o qual a próxima interrupção é considerada para indicar o início de um novo pacote de dispositivo (os pacotes parciais são descartados).</span><span class="sxs-lookup"><span data-stu-id="81bf6-503">Length of time after which the next interrupt is assumed to indicate the start of a new device packet (partial packets are discarded).</span></span> <span data-ttu-id="81bf6-504">No caso de uma interrupção ser perdida, isso permite que o driver de dispositivo apontador sincronize sua representação interna do estado do pacote com o estado do hardware.</span><span class="sxs-lookup"><span data-stu-id="81bf6-504">In the event that an interrupt is lost, this allows the pointing device driver to synchronize its internal representation of the packet state with the hardware state.</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="81bf6-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-506">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-508">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="81bf6-508">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-509">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-509">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="81bf6-510">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="81bf6-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="81bf6-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81bf6-512">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="81bf6-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="81bf6-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81bf6-514">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="81bf6-514">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="81bf6-515">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="81bf6-515">Name of the scoping system.</span></span>

<span data-ttu-id="81bf6-516">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81bf6-517">Comentários</span><span class="sxs-lookup"><span data-stu-id="81bf6-517">Remarks</span></span>

<span data-ttu-id="81bf6-518">A classe **Win32 \_ PointingDevice** é derivada de [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="81bf6-518">The **Win32\_PointingDevice** class is derived from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81bf6-519">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81bf6-519">Requirements</span></span>



| <span data-ttu-id="81bf6-520">Requisito</span><span class="sxs-lookup"><span data-stu-id="81bf6-520">Requirement</span></span> | <span data-ttu-id="81bf6-521">Valor</span><span class="sxs-lookup"><span data-stu-id="81bf6-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81bf6-522">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81bf6-522">Minimum supported client</span></span><br/> | <span data-ttu-id="81bf6-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81bf6-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81bf6-524">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81bf6-524">Minimum supported server</span></span><br/> | <span data-ttu-id="81bf6-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81bf6-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81bf6-526">Namespace</span><span class="sxs-lookup"><span data-stu-id="81bf6-526">Namespace</span></span><br/>                | <span data-ttu-id="81bf6-527">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="81bf6-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81bf6-528">MOF</span><span class="sxs-lookup"><span data-stu-id="81bf6-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81bf6-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81bf6-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81bf6-530">DLL</span><span class="sxs-lookup"><span data-stu-id="81bf6-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81bf6-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81bf6-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81bf6-532">Confira também</span><span class="sxs-lookup"><span data-stu-id="81bf6-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bf6-533">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="81bf6-533">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="81bf6-534">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="81bf6-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
