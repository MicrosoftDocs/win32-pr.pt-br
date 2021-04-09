---
description: Representa uma bateria conectada ao sistema de computador.
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Classe Win32_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010274"
---
# <a name="win32_battery-class"></a><span data-ttu-id="62183-103">\_Classe de bateria Win32</span><span class="sxs-lookup"><span data-stu-id="62183-103">Win32\_Battery class</span></span>

<span data-ttu-id="62183-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ da bateria do Win32** representa uma bateria conectada ao sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="62183-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="62183-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="62183-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="62183-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="62183-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62183-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62183-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
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

## <a name="members"></a><span data-ttu-id="62183-108">Membros</span><span class="sxs-lookup"><span data-stu-id="62183-108">Members</span></span>

<span data-ttu-id="62183-109">A classe de **\_ bateria do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="62183-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="62183-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="62183-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="62183-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62183-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="62183-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="62183-112">Methods</span></span>

<span data-ttu-id="62183-113">A classe de **\_ bateria do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="62183-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="62183-114">Método</span><span class="sxs-lookup"><span data-stu-id="62183-114">Method</span></span>            | <span data-ttu-id="62183-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="62183-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62183-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="62183-116">**Reset**</span></span>         | <span data-ttu-id="62183-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="62183-117">Not implemented.</span></span> <span data-ttu-id="62183-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) na [**\_ bateria do CIM**](cim-battery.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="62183-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="62183-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="62183-119">**SetPowerState**</span></span> | <span data-ttu-id="62183-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="62183-120">Not implemented.</span></span> <span data-ttu-id="62183-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) na [**\_ bateria CIM**](cim-battery.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="62183-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="62183-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62183-122">Properties</span></span>

<span data-ttu-id="62183-123">A classe de **\_ bateria do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62183-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62183-124">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="62183-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62183-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62183-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-127">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="62183-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="62183-128">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-128">Availability and status of the device.</span></span>

<span data-ttu-id="62183-129">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62183-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="62183-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62183-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="62183-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="62183-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="62183-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="62183-133">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="62183-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="62183-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="62183-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="62183-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="62183-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="62183-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="62183-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="62183-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="62183-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="62183-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="62183-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="62183-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="62183-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="62183-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="62183-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="62183-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="62183-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="62183-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="62183-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="62183-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="62183-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="62183-144">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="62183-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="62183-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="62183-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="62183-146">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="62183-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="62183-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="62183-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="62183-148">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="62183-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="62183-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="62183-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="62183-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="62183-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="62183-151">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="62183-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="62183-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="62183-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="62183-153">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="62183-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="62183-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="62183-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="62183-155">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="62183-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="62183-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="62183-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="62183-157">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="62183-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="62183-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="62183-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="62183-159">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="62183-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-160">**BatteryRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="62183-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-163">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("hKey \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| Recharger"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Minutes")</span><span class="sxs-lookup"><span data-stu-id="62183-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="62183-164">Tempo necessário para encarregar totalmente a bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="62183-165">Não há suporte a esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="62183-165">This property is not supported.</span></span> <span data-ttu-id="62183-166">**BatteryRechargeTime** não tem uma propriedade de substituição e agora é considerado obsoleto.</span><span class="sxs-lookup"><span data-stu-id="62183-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="62183-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="62183-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62183-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62183-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-170">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,14 ")</span><span class="sxs-lookup"><span data-stu-id="62183-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="62183-171">Status da bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-171">Status of the battery.</span></span> <span data-ttu-id="62183-172">O valor 10 (indefinido) não é válido no esquema CIM porque, no DMI, ele representa que nenhuma bateria está instalada.</span><span class="sxs-lookup"><span data-stu-id="62183-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="62183-173">Nesse caso, o objeto não deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="62183-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="62183-174">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62183-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="62183-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="62183-176">A bateria está descarregando.</span><span class="sxs-lookup"><span data-stu-id="62183-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62183-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="62183-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="62183-178">O sistema tem acesso ao AC, portanto nenhuma bateria está sendo descarregada.</span><span class="sxs-lookup"><span data-stu-id="62183-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="62183-179">No entanto, a bateria não está necessariamente carregando.</span><span class="sxs-lookup"><span data-stu-id="62183-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="62183-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Totalmente cobrado** (3)</span><span class="sxs-lookup"><span data-stu-id="62183-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="62183-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (4)</span><span class="sxs-lookup"><span data-stu-id="62183-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="62183-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="62183-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="62183-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Carregando** (6)</span><span class="sxs-lookup"><span data-stu-id="62183-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="62183-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Carregando e alto** (7)</span><span class="sxs-lookup"><span data-stu-id="62183-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="62183-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Carregando e baixo** (8)</span><span class="sxs-lookup"><span data-stu-id="62183-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="62183-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Cobrança e crítico** (9)</span><span class="sxs-lookup"><span data-stu-id="62183-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="62183-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (10)</span><span class="sxs-lookup"><span data-stu-id="62183-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="62183-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Parcialmente cobrado** (11)</span><span class="sxs-lookup"><span data-stu-id="62183-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-189">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="62183-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-192">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="62183-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="62183-193">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="62183-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="62183-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62183-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-195">**Química**</span><span class="sxs-lookup"><span data-stu-id="62183-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62183-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62183-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-198">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="62183-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="62183-199">Enumeração que descreve a química da bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="62183-200">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62183-201">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="62183-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62183-202">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="62183-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="62183-203">**Liderar Acid** (3)</span><span class="sxs-lookup"><span data-stu-id="62183-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="62183-204">**Níquel cádmio** (4)</span><span class="sxs-lookup"><span data-stu-id="62183-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="62183-205">**Hydride de metal de níquel** (5)</span><span class="sxs-lookup"><span data-stu-id="62183-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="62183-206">**Íon de** lítio (6)</span><span class="sxs-lookup"><span data-stu-id="62183-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="62183-207">**Ar Zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="62183-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="62183-208">**Polymer de lítio** (8)</span><span class="sxs-lookup"><span data-stu-id="62183-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-209">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="62183-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-210">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-212">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62183-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62183-213">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="62183-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="62183-214">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="62183-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="62183-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="62183-216"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="62183-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="62183-217">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="62183-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="62183-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="62183-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="62183-219">(1)</span><span class="sxs-lookup"><span data-stu-id="62183-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="62183-220">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="62183-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62183-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="62183-222">(2)</span><span class="sxs-lookup"><span data-stu-id="62183-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="62183-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="62183-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="62183-224">(3)</span><span class="sxs-lookup"><span data-stu-id="62183-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="62183-225">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="62183-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="62183-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="62183-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="62183-227">(4)</span><span class="sxs-lookup"><span data-stu-id="62183-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="62183-228">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="62183-228">Device is not working properly.</span></span> <span data-ttu-id="62183-229">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="62183-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="62183-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="62183-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="62183-231">(5)</span><span class="sxs-lookup"><span data-stu-id="62183-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="62183-232">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="62183-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="62183-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="62183-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="62183-234"> (6)</span><span class="sxs-lookup"><span data-stu-id="62183-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="62183-235">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="62183-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="62183-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="62183-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="62183-237">(7)</span><span class="sxs-lookup"><span data-stu-id="62183-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="62183-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="62183-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="62183-239">(8)</span><span class="sxs-lookup"><span data-stu-id="62183-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="62183-240">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="62183-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="62183-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="62183-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="62183-242">(9)</span><span class="sxs-lookup"><span data-stu-id="62183-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="62183-243">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="62183-243">Device is not working properly.</span></span> <span data-ttu-id="62183-244">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="62183-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="62183-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="62183-246">(10)</span><span class="sxs-lookup"><span data-stu-id="62183-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="62183-247">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="62183-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="62183-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="62183-249">(11)</span><span class="sxs-lookup"><span data-stu-id="62183-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="62183-250">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="62183-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="62183-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="62183-252">12</span><span class="sxs-lookup"><span data-stu-id="62183-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="62183-253">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="62183-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="62183-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="62183-255">(13)</span><span class="sxs-lookup"><span data-stu-id="62183-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="62183-256">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="62183-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="62183-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="62183-258">(14)</span><span class="sxs-lookup"><span data-stu-id="62183-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="62183-259">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="62183-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="62183-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="62183-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="62183-261">(15)</span><span class="sxs-lookup"><span data-stu-id="62183-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="62183-262">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="62183-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="62183-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="62183-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="62183-264">(16)</span><span class="sxs-lookup"><span data-stu-id="62183-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="62183-265">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="62183-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="62183-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="62183-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="62183-267">(17)</span><span class="sxs-lookup"><span data-stu-id="62183-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="62183-268">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="62183-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62183-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="62183-270">(18)</span><span class="sxs-lookup"><span data-stu-id="62183-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="62183-271">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="62183-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="62183-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="62183-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="62183-273">(19)</span><span class="sxs-lookup"><span data-stu-id="62183-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="62183-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="62183-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="62183-275">(20)</span><span class="sxs-lookup"><span data-stu-id="62183-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="62183-276">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="62183-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="62183-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="62183-278">(21)</span><span class="sxs-lookup"><span data-stu-id="62183-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="62183-279">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="62183-279">System failure.</span></span> <span data-ttu-id="62183-280">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="62183-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="62183-281">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="62183-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="62183-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="62183-283">(22)</span><span class="sxs-lookup"><span data-stu-id="62183-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="62183-284">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="62183-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="62183-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="62183-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="62183-286">(23)</span><span class="sxs-lookup"><span data-stu-id="62183-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="62183-287">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="62183-287">System failure.</span></span> <span data-ttu-id="62183-288">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="62183-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="62183-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="62183-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="62183-290">(24)</span><span class="sxs-lookup"><span data-stu-id="62183-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="62183-291">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="62183-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="62183-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="62183-293">(25)</span><span class="sxs-lookup"><span data-stu-id="62183-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="62183-294">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="62183-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="62183-296">(26)</span><span class="sxs-lookup"><span data-stu-id="62183-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="62183-297">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62183-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="62183-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="62183-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="62183-299">(27)</span><span class="sxs-lookup"><span data-stu-id="62183-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="62183-300">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="62183-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="62183-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="62183-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="62183-302">(28)</span><span class="sxs-lookup"><span data-stu-id="62183-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="62183-303">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="62183-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="62183-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="62183-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="62183-305">(29)</span><span class="sxs-lookup"><span data-stu-id="62183-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="62183-306">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="62183-306">Device is disabled.</span></span> <span data-ttu-id="62183-307">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="62183-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="62183-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="62183-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="62183-309">(30)</span><span class="sxs-lookup"><span data-stu-id="62183-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="62183-310">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="62183-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62183-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62183-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="62183-312">(31)</span><span class="sxs-lookup"><span data-stu-id="62183-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="62183-313">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="62183-313">Device is not working properly.</span></span> <span data-ttu-id="62183-314">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="62183-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-315">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="62183-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-316">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62183-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62183-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-318">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62183-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62183-319">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="62183-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="62183-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-321">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62183-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-324">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62183-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62183-325">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="62183-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="62183-326">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="62183-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="62183-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-328">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62183-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-331">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="62183-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="62183-332">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="62183-332">Description of the object.</span></span>

<span data-ttu-id="62183-333">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62183-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-334">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="62183-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-hours ")</span><span class="sxs-lookup"><span data-stu-id="62183-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="62183-338">Crie a capacidade da bateria em milliwatt-hours.</span><span class="sxs-lookup"><span data-stu-id="62183-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="62183-339">Se não houver suporte para a propriedade, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="62183-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="62183-340">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-341">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="62183-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62183-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62183-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-344">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="62183-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="62183-345">Voltagem de design da bateria em milivolts.</span><span class="sxs-lookup"><span data-stu-id="62183-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="62183-346">Se não houver suporte para o atributo, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="62183-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="62183-347">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="62183-348">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="62183-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="62183-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="62183-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-352">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62183-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62183-353">Identifica a bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-353">Identifies the battery.</span></span>

<span data-ttu-id="62183-354">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="62183-355">Exemplo: "bateria interna"</span><span class="sxs-lookup"><span data-stu-id="62183-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="62183-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="62183-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-357">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62183-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62183-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62183-359">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="62183-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="62183-360">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="62183-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-362">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62183-364">Cadeia de caracteres de forma livre que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="62183-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="62183-365">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-366">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="62183-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-367">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62183-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62183-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-369">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span><span class="sxs-lookup"><span data-stu-id="62183-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="62183-370">Estimativa da porcentagem de carga total restante.</span><span class="sxs-lookup"><span data-stu-id="62183-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="62183-371">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="62183-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-373">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-375">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="62183-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="62183-376">Estimativa em minutos do tempo para o esgotamento de carga da bateria sob as condições de carregamento presentes, se a energia do utilitário estiver desligada ou perdida e permanecer desligada ou se um laptop estiver desconectado de uma fonte de alimentação.</span><span class="sxs-lookup"><span data-stu-id="62183-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="62183-377">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-378">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="62183-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-379">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-381">Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("hKey \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="62183-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="62183-382">Quantidade de tempo necessário para drenar completamente a bateria depois que ela é totalmente carregada.</span><span class="sxs-lookup"><span data-stu-id="62183-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="62183-383">Essa propriedade não é mais usada e é considerada obsoleta.</span><span class="sxs-lookup"><span data-stu-id="62183-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="62183-384">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="62183-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-385">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-387">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="62183-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="62183-388">Tempo de vida esperado da bateria em minutos, supondo que a bateria seja totalmente carregada.</span><span class="sxs-lookup"><span data-stu-id="62183-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="62183-389">A propriedade representa a vida útil total esperada da bateria, não sua vida útil atual, que é indicada pela propriedade **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="62183-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="62183-390">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-391">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="62183-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-392">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-hours ")</span><span class="sxs-lookup"><span data-stu-id="62183-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="62183-395">Capacidade de carga total da bateria em milliwatt-horas.</span><span class="sxs-lookup"><span data-stu-id="62183-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="62183-396">A comparação do valor com a propriedade **DesignCapacity** determina quando a bateria requer substituição.</span><span class="sxs-lookup"><span data-stu-id="62183-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="62183-397">O fim da vida útil de uma bateria é normalmente quando a propriedade **FullChargeCapacity** cai abaixo de 80% da propriedade **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="62183-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="62183-398">Se não houver suporte para a propriedade, insira 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="62183-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="62183-399">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62183-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-401">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62183-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62183-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-403">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="62183-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="62183-404">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="62183-404">Date and time the object was installed.</span></span> <span data-ttu-id="62183-405">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="62183-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="62183-406">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62183-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-407">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="62183-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-408">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62183-410">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62183-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="62183-411">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-412">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="62183-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-413">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-415">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="62183-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="62183-416">Tempo máximo, em minutos, para encarregar totalmente a bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="62183-417">A propriedade representa o tempo de recarga de uma bateria totalmente descarregada, não o tempo de encargo restante atual, que é indicado na propriedade **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="62183-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="62183-418">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-419">**Nome**</span><span class="sxs-lookup"><span data-stu-id="62183-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-422">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="62183-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="62183-423">Define o rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="62183-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="62183-424">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="62183-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="62183-425">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62183-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="62183-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-429">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62183-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62183-430">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62183-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="62183-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="62183-432">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="62183-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="62183-433">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="62183-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-434">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62183-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62183-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62183-436">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62183-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="62183-437">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="62183-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62183-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="62183-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="62183-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="62183-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="62183-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="62183-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="62183-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="62183-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="62183-442">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="62183-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="62183-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="62183-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="62183-444">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="62183-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="62183-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="62183-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="62183-446">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="62183-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="62183-447">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="62183-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="62183-448">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="62183-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="62183-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="62183-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="62183-450">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="62183-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="62183-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="62183-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="62183-452">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="62183-452">Timed Power-On Supported</span></span>

<span data-ttu-id="62183-453">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="62183-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-454">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="62183-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-455">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62183-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62183-456">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62183-457">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="62183-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="62183-458">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="62183-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="62183-459">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-460">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="62183-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-461">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-462">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-463">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,10 ")</span><span class="sxs-lookup"><span data-stu-id="62183-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="62183-464">Número de versão da especificação de dados com suporte da bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="62183-465">Se a bateria não oferecer suporte a essa função, o valor deverá ser deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="62183-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="62183-466">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-467">**Status**</span><span class="sxs-lookup"><span data-stu-id="62183-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-468">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-470">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="62183-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="62183-471">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="62183-471">Current status of the object.</span></span> <span data-ttu-id="62183-472">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="62183-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="62183-473">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="62183-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="62183-474">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="62183-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="62183-475">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="62183-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="62183-476">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="62183-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="62183-477">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62183-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="62183-478">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="62183-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="62183-479">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="62183-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="62183-480">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="62183-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="62183-481">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="62183-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62183-482">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="62183-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="62183-483">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="62183-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="62183-484">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="62183-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="62183-485">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="62183-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="62183-486">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="62183-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="62183-487">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="62183-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="62183-488">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="62183-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="62183-489">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="62183-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="62183-490">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="62183-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="62183-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-492">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62183-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62183-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-494">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="62183-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="62183-495">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62183-495">State of the logical device.</span></span> <span data-ttu-id="62183-496">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="62183-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="62183-497">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62183-498">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="62183-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62183-499">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="62183-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="62183-500">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="62183-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="62183-501">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="62183-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="62183-502">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="62183-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62183-503">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62183-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-504">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-506">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62183-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62183-507">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="62183-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="62183-508">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-509">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="62183-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-510">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62183-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62183-511">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-512">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62183-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62183-513">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="62183-513">Name of the scoping system.</span></span>

<span data-ttu-id="62183-514">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-515">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="62183-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-516">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-517">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-518">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="62183-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="62183-519">Tempo decorrido em segundos desde a última vez em que o UPS do sistema de computador mudou para a energia da bateria ou o tempo desde que o sistema ou o no-break foi reiniciado pela última vez, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="62183-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="62183-520">Se a bateria estiver "na linha", 0 (zero) será retornado.</span><span class="sxs-lookup"><span data-stu-id="62183-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="62183-521">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="62183-522">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="62183-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62183-523">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62183-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62183-524">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62183-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62183-525">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="62183-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="62183-526">Tempo restante para cobrar totalmente a bateria em minutos na taxa de carregamento e no uso atuais.</span><span class="sxs-lookup"><span data-stu-id="62183-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="62183-527">Essa propriedade é herdada [**da \_ bateria CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="62183-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62183-528">Comentários</span><span class="sxs-lookup"><span data-stu-id="62183-528">Remarks</span></span>

<span data-ttu-id="62183-529">A classe de **\_ bateria do Win32** é derivada da [**\_ bateria CIM**](cim-battery.md) que deriva [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62183-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="62183-530">O Windows Server 2008 contém os drivers de UPS (APC) no sistema operacional, que permite que você trate os UPS como uma fonte de bateria.</span><span class="sxs-lookup"><span data-stu-id="62183-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="62183-531">Isso permite que você monitore o status de UPS usando um script e execute ações quando necessário.</span><span class="sxs-lookup"><span data-stu-id="62183-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="62183-532">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62183-532">Examples</span></span>

<span data-ttu-id="62183-533">O exemplo de código do [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell consulta a **\_ bateria do Win32** para determinar se deseja ou não ativar ou desativar a conexão sem fio para economizar energia.</span><span class="sxs-lookup"><span data-stu-id="62183-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="62183-534">A amostra de [informações da lista de UPS](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) do Perl lista informações sobre as fontes de energia ininterrupta anexadas a um computador.</span><span class="sxs-lookup"><span data-stu-id="62183-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="62183-535">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62183-535">Requirements</span></span>



| <span data-ttu-id="62183-536">Requisito</span><span class="sxs-lookup"><span data-stu-id="62183-536">Requirement</span></span> | <span data-ttu-id="62183-537">Valor</span><span class="sxs-lookup"><span data-stu-id="62183-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62183-538">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62183-538">Minimum supported client</span></span><br/> | <span data-ttu-id="62183-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62183-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62183-540">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62183-540">Minimum supported server</span></span><br/> | <span data-ttu-id="62183-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62183-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62183-542">Namespace</span><span class="sxs-lookup"><span data-stu-id="62183-542">Namespace</span></span><br/>                | <span data-ttu-id="62183-543">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="62183-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62183-544">MOF</span><span class="sxs-lookup"><span data-stu-id="62183-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62183-545"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62183-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62183-546">DLL</span><span class="sxs-lookup"><span data-stu-id="62183-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62183-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62183-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62183-548">Confira também</span><span class="sxs-lookup"><span data-stu-id="62183-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62183-549">**\_Bateria CIM**</span><span class="sxs-lookup"><span data-stu-id="62183-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="62183-550">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="62183-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

