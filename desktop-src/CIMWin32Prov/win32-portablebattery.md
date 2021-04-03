---
description: A \_ classe WMI PortableBattery do Win32 contém as propriedades relacionadas a uma bateria portátil, como uma bateria de computador notebook.
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Classe Win32_PortableBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646252"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="5f142-103">\_Classe Win32 PortableBattery</span><span class="sxs-lookup"><span data-stu-id="5f142-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="5f142-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortableBattery do Win32** contém as propriedades relacionadas a uma bateria portátil, como uma bateria de computador notebook.</span><span class="sxs-lookup"><span data-stu-id="5f142-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="5f142-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5f142-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5f142-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="5f142-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f142-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f142-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="5f142-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5f142-108">Members</span></span>

<span data-ttu-id="5f142-109">A classe **Win32 \_ PortableBattery** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f142-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="5f142-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f142-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5f142-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f142-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5f142-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f142-112">Methods</span></span>

<span data-ttu-id="5f142-113">A classe **Win32 \_ PortableBattery** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5f142-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="5f142-114">Método</span><span class="sxs-lookup"><span data-stu-id="5f142-114">Method</span></span>            | <span data-ttu-id="5f142-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f142-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f142-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="5f142-116">**Reset**</span></span>         | <span data-ttu-id="5f142-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5f142-117">Not implemented.</span></span> <span data-ttu-id="5f142-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) na [**\_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="5f142-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5f142-119">**SetPowerState**</span></span> | <span data-ttu-id="5f142-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5f142-120">Not implemented.</span></span> <span data-ttu-id="5f142-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) na [**\_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5f142-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f142-122">Properties</span></span>

<span data-ttu-id="5f142-123">A classe **Win32 \_ PortableBattery** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f142-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f142-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="5f142-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5f142-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-128">Availability and status of the device.</span></span>

<span data-ttu-id="5f142-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f142-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5f142-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f142-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5f142-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5f142-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5f142-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="5f142-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5f142-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="5f142-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5f142-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="5f142-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5f142-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="5f142-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5f142-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="5f142-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5f142-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="5f142-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5f142-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="5f142-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5f142-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5f142-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5f142-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5f142-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5f142-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="5f142-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5f142-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="5f142-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5f142-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5f142-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="5f142-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="5f142-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5f142-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5f142-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5f142-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="5f142-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5f142-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="5f142-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5f142-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5f142-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5f142-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="5f142-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5f142-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="5f142-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="5f142-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5f142-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5f142-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="5f142-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5f142-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="5f142-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="5f142-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="5f142-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-161">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-163">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,14 ")</span><span class="sxs-lookup"><span data-stu-id="5f142-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-164">Descrição do status de cobrança da bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-164">Description of the battery's charge status.</span></span> <span data-ttu-id="5f142-165">O valor 10 (indefinido) não é válido no esquema de modelo CIM (CIM) porque, no Desktop Management Interface (DMI), ele indica que nenhuma bateria está instalada.</span><span class="sxs-lookup"><span data-stu-id="5f142-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="5f142-166">Nesse caso, esse objeto não deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="5f142-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="5f142-167">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f142-168">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5f142-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f142-169">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5f142-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="5f142-170">**Totalmente cobrado** (3)</span><span class="sxs-lookup"><span data-stu-id="5f142-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="5f142-171">**Baixo** (4)</span><span class="sxs-lookup"><span data-stu-id="5f142-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5f142-172">**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="5f142-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="5f142-173">**Carregando** (6)</span><span class="sxs-lookup"><span data-stu-id="5f142-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="5f142-174">**Carregando e alto** (7)</span><span class="sxs-lookup"><span data-stu-id="5f142-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="5f142-175">**Carregando e baixo** (8)</span><span class="sxs-lookup"><span data-stu-id="5f142-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="5f142-176">**Cobrança e crítico** (9)</span><span class="sxs-lookup"><span data-stu-id="5f142-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5f142-177">**Indefinido** (10)</span><span class="sxs-lookup"><span data-stu-id="5f142-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="5f142-178">**Parcialmente cobrado** (11)</span><span class="sxs-lookup"><span data-stu-id="5f142-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-179">**CapacityMultiplier**</span><span class="sxs-lookup"><span data-stu-id="5f142-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-180">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-182">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 22 \| multiplicador de capacidade de design")</span><span class="sxs-lookup"><span data-stu-id="5f142-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-183">Fator de multiplicação do valor de **DesignCapacity** para garantir que o valor de hora de milliwatt não ultrapasse as implementações de SBDS (especificação de dados da bateria inteligente).</span><span class="sxs-lookup"><span data-stu-id="5f142-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="5f142-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5f142-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-187">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5f142-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-188">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="5f142-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="5f142-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-190">**Química**</span><span class="sxs-lookup"><span data-stu-id="5f142-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-193">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="5f142-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-194">Química da bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-194">Chemistry of the battery.</span></span>

<span data-ttu-id="5f142-195">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f142-196">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5f142-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f142-197">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5f142-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="5f142-198">**Liderar Acid** (3)</span><span class="sxs-lookup"><span data-stu-id="5f142-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="5f142-199">**Níquel cádmio** (4)</span><span class="sxs-lookup"><span data-stu-id="5f142-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="5f142-200">**Hydride de metal de níquel** (5)</span><span class="sxs-lookup"><span data-stu-id="5f142-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="5f142-201">**Íon de** lítio (6)</span><span class="sxs-lookup"><span data-stu-id="5f142-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="5f142-202">**Ar Zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="5f142-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="5f142-203">**Polymer de lítio** (8)</span><span class="sxs-lookup"><span data-stu-id="5f142-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-204">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5f142-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-205">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-207">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5f142-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-208">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5f142-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5f142-209">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5f142-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5f142-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5f142-211"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="5f142-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-212">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5f142-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5f142-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5f142-214">(1)</span><span class="sxs-lookup"><span data-stu-id="5f142-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-215">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5f142-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5f142-217">(2)</span><span class="sxs-lookup"><span data-stu-id="5f142-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5f142-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5f142-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5f142-219">(3)</span><span class="sxs-lookup"><span data-stu-id="5f142-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-220">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="5f142-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5f142-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5f142-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5f142-222">(4)</span><span class="sxs-lookup"><span data-stu-id="5f142-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-223">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-223">Device is not working properly.</span></span> <span data-ttu-id="5f142-224">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5f142-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5f142-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="5f142-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5f142-226">(5)</span><span class="sxs-lookup"><span data-stu-id="5f142-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-227">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="5f142-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5f142-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5f142-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5f142-229"> (6)</span><span class="sxs-lookup"><span data-stu-id="5f142-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-230">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5f142-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5f142-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5f142-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5f142-232">(7)</span><span class="sxs-lookup"><span data-stu-id="5f142-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5f142-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="5f142-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5f142-234">(8)</span><span class="sxs-lookup"><span data-stu-id="5f142-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-235">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="5f142-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5f142-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="5f142-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5f142-237">(9)</span><span class="sxs-lookup"><span data-stu-id="5f142-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-238">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-238">Device is not working properly.</span></span> <span data-ttu-id="5f142-239">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5f142-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="5f142-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5f142-241">(10)</span><span class="sxs-lookup"><span data-stu-id="5f142-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-242">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5f142-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="5f142-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5f142-244">(11)</span><span class="sxs-lookup"><span data-stu-id="5f142-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-245">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5f142-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="5f142-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5f142-247">12</span><span class="sxs-lookup"><span data-stu-id="5f142-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-248">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="5f142-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5f142-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5f142-250">(13)</span><span class="sxs-lookup"><span data-stu-id="5f142-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-251">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5f142-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="5f142-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5f142-253">(14)</span><span class="sxs-lookup"><span data-stu-id="5f142-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-254">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5f142-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5f142-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="5f142-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5f142-256">(15)</span><span class="sxs-lookup"><span data-stu-id="5f142-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-257">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="5f142-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5f142-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="5f142-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5f142-259">(16)</span><span class="sxs-lookup"><span data-stu-id="5f142-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-260">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="5f142-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5f142-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="5f142-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5f142-262">(17)</span><span class="sxs-lookup"><span data-stu-id="5f142-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-263">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5f142-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5f142-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5f142-265">(18)</span><span class="sxs-lookup"><span data-stu-id="5f142-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-266">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="5f142-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5f142-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="5f142-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5f142-268">(19)</span><span class="sxs-lookup"><span data-stu-id="5f142-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5f142-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5f142-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5f142-270">(20)</span><span class="sxs-lookup"><span data-stu-id="5f142-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-271">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5f142-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5f142-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5f142-273">(21)</span><span class="sxs-lookup"><span data-stu-id="5f142-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-274">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5f142-274">System failure.</span></span> <span data-ttu-id="5f142-275">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5f142-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5f142-276">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5f142-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5f142-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5f142-278">(22)</span><span class="sxs-lookup"><span data-stu-id="5f142-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-279">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5f142-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5f142-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="5f142-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5f142-281">(23)</span><span class="sxs-lookup"><span data-stu-id="5f142-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-282">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5f142-282">System failure.</span></span> <span data-ttu-id="5f142-283">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5f142-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5f142-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="5f142-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5f142-285">(24)</span><span class="sxs-lookup"><span data-stu-id="5f142-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-286">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="5f142-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5f142-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5f142-288">(25)</span><span class="sxs-lookup"><span data-stu-id="5f142-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-289">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5f142-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5f142-291">(26)</span><span class="sxs-lookup"><span data-stu-id="5f142-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-292">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f142-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5f142-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="5f142-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5f142-294">(27)</span><span class="sxs-lookup"><span data-stu-id="5f142-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-295">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="5f142-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5f142-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="5f142-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5f142-297">(28)</span><span class="sxs-lookup"><span data-stu-id="5f142-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-298">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="5f142-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5f142-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="5f142-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5f142-300">(29)</span><span class="sxs-lookup"><span data-stu-id="5f142-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-301">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5f142-301">Device is disabled.</span></span> <span data-ttu-id="5f142-302">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="5f142-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5f142-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5f142-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5f142-304">(30)</span><span class="sxs-lookup"><span data-stu-id="5f142-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-305">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5f142-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5f142-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5f142-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5f142-307">(31)</span><span class="sxs-lookup"><span data-stu-id="5f142-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-308">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-308">Device is not working properly.</span></span> <span data-ttu-id="5f142-309">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="5f142-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-310">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5f142-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-311">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5f142-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-313">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5f142-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-314">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5f142-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5f142-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5f142-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-319">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5f142-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5f142-320">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5f142-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5f142-321">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5f142-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5f142-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-323">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5f142-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-326">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5f142-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-327">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5f142-327">Description of the object.</span></span>

<span data-ttu-id="5f142-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-329">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="5f142-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-330">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-332">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milliwatt-hours ")</span><span class="sxs-lookup"><span data-stu-id="5f142-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-333">Crie a capacidade da bateria em milliwatt-hours.</span><span class="sxs-lookup"><span data-stu-id="5f142-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="5f142-334">Se não houver suporte para essa propriedade, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5f142-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="5f142-335">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-336">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="5f142-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-337">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5f142-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-339">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,9 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="5f142-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-340">Voltagem de design da bateria em milivolts.</span><span class="sxs-lookup"><span data-stu-id="5f142-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="5f142-341">Se não houver suporte para esse atributo, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5f142-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="5f142-342">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="5f142-343">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-344">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5f142-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-347">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="5f142-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-348">Identificador da bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-348">Battery identifier.</span></span>

<span data-ttu-id="5f142-349">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5f142-350">Exemplo: "bateria interna"</span><span class="sxs-lookup"><span data-stu-id="5f142-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="5f142-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5f142-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-352">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5f142-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f142-354">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="5f142-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="5f142-355">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5f142-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-357">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f142-359">Mais informações sobre o erro registrado em **LastErrorCode** e as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="5f142-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="5f142-360">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-361">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="5f142-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-362">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-364">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("percent")</span><span class="sxs-lookup"><span data-stu-id="5f142-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-365">Estimativa da porcentagem de carga total restante.</span><span class="sxs-lookup"><span data-stu-id="5f142-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="5f142-366">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="5f142-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-368">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-370">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,15 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="5f142-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-371">Estimativa em minutos do tempo para o esgotamento de carga da bateria sob as condições de carregamento presentes, se a energia do utilitário estiver desligada ou perdida e permanecer desligada ou se um laptop estiver desconectado de uma fonte de alimentação.</span><span class="sxs-lookup"><span data-stu-id="5f142-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="5f142-372">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-373">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="5f142-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-374">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f142-376">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="5f142-376">Not supported.</span></span>

<span data-ttu-id="5f142-377">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-378">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="5f142-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-379">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-381">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="5f142-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-382">Tempo de vida esperado da bateria em minutos, supondo que a bateria seja totalmente carregada.</span><span class="sxs-lookup"><span data-stu-id="5f142-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="5f142-383">Essa propriedade representa a vida útil total esperada da bateria, não sua vida útil atual, que é indicada pela propriedade **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="5f142-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="5f142-384">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-385">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="5f142-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-386">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-388">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milliwatt-hours ")</span><span class="sxs-lookup"><span data-stu-id="5f142-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-389">Capacidade de carga total da bateria em milliwatt-horas.</span><span class="sxs-lookup"><span data-stu-id="5f142-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="5f142-390">A comparação desse valor com a propriedade **DesignCapacity** determina quando a bateria requer substituição.</span><span class="sxs-lookup"><span data-stu-id="5f142-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="5f142-391">O fim da vida útil de uma bateria é normalmente quando a propriedade **FullChargeCapacity** cai abaixo de 80% da propriedade **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="5f142-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="5f142-392">Se não houver suporte para essa propriedade, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5f142-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="5f142-393">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5f142-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-395">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f142-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-397">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5f142-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-398">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5f142-398">Date and time the object was installed.</span></span> <span data-ttu-id="5f142-399">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5f142-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5f142-400">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-401">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5f142-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-402">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f142-404">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5f142-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5f142-405">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-406">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="5f142-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-407">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-409">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| local do tipo SMBIOS 22 \| ")</span><span class="sxs-lookup"><span data-stu-id="5f142-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-410">Local físico da bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-410">Physical location of the battery.</span></span> <span data-ttu-id="5f142-411">Essa propriedade é preenchida pelo fabricante do computador.</span><span class="sxs-lookup"><span data-stu-id="5f142-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="5f142-412">Exemplo: "na parte posterior, à esquerda"</span><span class="sxs-lookup"><span data-stu-id="5f142-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="5f142-413">**Fabricado**</span><span class="sxs-lookup"><span data-stu-id="5f142-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-414">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-416">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS de \| data de fabricação")</span><span class="sxs-lookup"><span data-stu-id="5f142-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-417">Data em que a bateria foi fabricada.</span><span class="sxs-lookup"><span data-stu-id="5f142-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="5f142-418">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5f142-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-419">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-421">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| fabricante do tipo SMBIOS 22 \| ")</span><span class="sxs-lookup"><span data-stu-id="5f142-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-422">Fabricante da bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="5f142-423">**MaxBatteryError**</span><span class="sxs-lookup"><span data-stu-id="5f142-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-424">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-426">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 22 \| erro máximo nos dados da bateria"), [**unidades**](../wmisdk/standard-qualifiers.md) ("porcentagem")</span><span class="sxs-lookup"><span data-stu-id="5f142-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-427">Diferença entre a maior quantidade estimada de energia restante na bateria e a quantidade atual relatada pela bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="5f142-428">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="5f142-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-429">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-431">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="5f142-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-432">Tempo máximo, em minutos, para encarregar totalmente a bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="5f142-433">Essa propriedade representa o tempo para recarregar uma bateria totalmente descarregada, não a hora de cobrança restante atual, que é indicada na propriedade **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="5f142-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="5f142-434">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-435">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5f142-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-438">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5f142-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-439">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5f142-439">Label by which the object is known.</span></span> <span data-ttu-id="5f142-440">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5f142-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5f142-441">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5f142-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-445">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5f142-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-446">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5f142-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5f142-447">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5f142-448">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5f142-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5f142-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5f142-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-450">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5f142-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f142-452">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5f142-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5f142-453">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="5f142-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f142-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5f142-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5f142-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5f142-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5f142-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5f142-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5f142-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5f142-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-458">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5f142-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5f142-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5f142-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-460">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="5f142-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5f142-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="5f142-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-462">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5f142-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5f142-463">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="5f142-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5f142-464">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5f142-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="5f142-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-466">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="5f142-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5f142-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="5f142-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5f142-468">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="5f142-468">Timed Power-On Supported</span></span>

<span data-ttu-id="5f142-469">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="5f142-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5f142-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-471">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5f142-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f142-473">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="5f142-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="5f142-474">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="5f142-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="5f142-475">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-476">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="5f142-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-477">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-479">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,10 ")</span><span class="sxs-lookup"><span data-stu-id="5f142-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-480">Número de versão da especificação de dados da bateria inteligente com suporte nesta bateria.</span><span class="sxs-lookup"><span data-stu-id="5f142-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="5f142-481">Se a bateria não oferecer suporte a essa função, o valor deverá ser deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="5f142-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="5f142-482">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-483">**Status**</span><span class="sxs-lookup"><span data-stu-id="5f142-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-485">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-486">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="5f142-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-487">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5f142-487">Current status of the object.</span></span> <span data-ttu-id="5f142-488">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="5f142-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5f142-489">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5f142-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5f142-490">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5f142-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5f142-491">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5f142-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5f142-492">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5f142-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5f142-493">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5f142-494">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5f142-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5f142-495">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5f142-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5f142-496">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5f142-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5f142-497">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5f142-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f142-498">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5f142-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5f142-499">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5f142-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5f142-500">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5f142-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5f142-501">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5f142-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5f142-502">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5f142-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5f142-503">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5f142-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5f142-504">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5f142-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5f142-505">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5f142-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5f142-506">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5f142-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5f142-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-508">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5f142-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-510">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="5f142-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-511">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5f142-511">State of the logical device.</span></span> <span data-ttu-id="5f142-512">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="5f142-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5f142-513">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f142-514">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5f142-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f142-515">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5f142-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5f142-516">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5f142-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5f142-517">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5f142-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5f142-518">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="5f142-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f142-519">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5f142-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-520">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-521">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-522">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5f142-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5f142-523">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="5f142-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="5f142-524">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-525">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5f142-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-526">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f142-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-527">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-528">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5f142-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5f142-529">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5f142-529">Name of the scoping system.</span></span>

<span data-ttu-id="5f142-530">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-531">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="5f142-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-532">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-533">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-534">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="5f142-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-535">Tempo decorrido em segundos desde a última vez em que o UPS do sistema de computador mudou para a energia da bateria ou o tempo desde que o sistema ou o no-break foi reiniciado pela última vez, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="5f142-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="5f142-536">Se a bateria estiver online, será retornado 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5f142-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="5f142-537">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f142-538">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="5f142-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f142-539">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f142-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f142-540">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f142-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f142-541">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Bateria portátil DMTF \| 2,16 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="5f142-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="5f142-542">Tempo restante em minutos para cobrar total da bateria na taxa de cobrança e no uso atuais.</span><span class="sxs-lookup"><span data-stu-id="5f142-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="5f142-543">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f142-544">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f142-544">Remarks</span></span>

<span data-ttu-id="5f142-545">A classe **Win32 \_ PortableBattery** é derivada da [**\_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="5f142-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f142-546">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f142-546">Requirements</span></span>



| <span data-ttu-id="5f142-547">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f142-547">Requirement</span></span> | <span data-ttu-id="5f142-548">Valor</span><span class="sxs-lookup"><span data-stu-id="5f142-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f142-549">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f142-549">Minimum supported client</span></span><br/> | <span data-ttu-id="5f142-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f142-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f142-551">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f142-551">Minimum supported server</span></span><br/> | <span data-ttu-id="5f142-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f142-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f142-553">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f142-553">Namespace</span></span><br/>                | <span data-ttu-id="5f142-554">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5f142-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f142-555">MOF</span><span class="sxs-lookup"><span data-stu-id="5f142-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f142-556"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f142-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f142-557">DLL</span><span class="sxs-lookup"><span data-stu-id="5f142-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f142-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f142-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f142-559">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f142-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f142-560">**\_Bateria CIM**</span><span class="sxs-lookup"><span data-stu-id="5f142-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="5f142-561">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="5f142-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
