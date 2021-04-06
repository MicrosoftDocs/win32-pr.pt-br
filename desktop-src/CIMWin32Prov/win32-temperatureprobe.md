---
description: O Win32 \_ TemperatureProbe&\# 32; Classe WMI representa as propriedades de um sensor de temperatura (termômetro eletrônico).
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Classe Win32_TemperatureProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826407"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="6344d-103">\_Classe Win32 TemperatureProbe</span><span class="sxs-lookup"><span data-stu-id="6344d-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="6344d-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ TemperatureProbe do Win32** representa as propriedades de um sensor de temperatura (termômetro eletrônico).</span><span class="sxs-lookup"><span data-stu-id="6344d-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="6344d-105">A maioria das informações fornecidas pela classe WMI **\_ TemperatureProbe do Win32** vem do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6344d-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="6344d-106">Leituras em tempo real para a propriedade **CurrentReading** não podem ser extraídas de tabelas SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="6344d-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="6344d-107">Por esse motivo, as implementações atuais do WMI não preenchem a propriedade **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="6344d-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="6344d-108">A presença da propriedade **CurrentReading** é reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6344d-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="6344d-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6344d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6344d-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6344d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6344d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6344d-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="6344d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="6344d-112">Members</span></span>

<span data-ttu-id="6344d-113">A classe **Win32 \_ TemperatureProbe** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6344d-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="6344d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6344d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6344d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6344d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6344d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6344d-116">Methods</span></span>

<span data-ttu-id="6344d-117">A classe **Win32 \_ TemperatureProbe** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6344d-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="6344d-118">Método</span><span class="sxs-lookup"><span data-stu-id="6344d-118">Method</span></span>            | <span data-ttu-id="6344d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="6344d-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6344d-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="6344d-120">**Reset**</span></span>         | <span data-ttu-id="6344d-121">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6344d-121">Not implemented.</span></span> <span data-ttu-id="6344d-122">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-temperaturesensor.md) no [**CIM \_ sensor**](cim-temperaturesensor.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="6344d-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="6344d-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6344d-123">**SetPowerState**</span></span> | <span data-ttu-id="6344d-124">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6344d-124">Not implemented.</span></span> <span data-ttu-id="6344d-125">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) no [**CIM \_ sensor**](cim-temperaturesensor.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="6344d-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6344d-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6344d-126">Properties</span></span>

<span data-ttu-id="6344d-127">A classe **Win32 \_ TemperatureProbe** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6344d-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6344d-128">**Correta**</span><span class="sxs-lookup"><span data-stu-id="6344d-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-131">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Investigação de temperatura de DMTF \| \| 1,19 ")</span><span class="sxs-lookup"><span data-stu-id="6344d-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-132">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="6344d-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="6344d-133">Seu valor é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="6344d-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="6344d-134">A precisão, a resolução e a tolerância são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="6344d-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6344d-135">A precisão pode variar e depende se o dispositivo é linear ou não por seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6344d-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6344d-136">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-137">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="6344d-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6344d-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-140">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6344d-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-141">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-141">Availability and status of the device.</span></span>

<span data-ttu-id="6344d-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6344d-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6344d-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6344d-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="6344d-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6344d-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="6344d-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6344d-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="6344d-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6344d-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="6344d-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6344d-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="6344d-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6344d-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="6344d-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6344d-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="6344d-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-151">Offline</span><span class="sxs-lookup"><span data-stu-id="6344d-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6344d-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="6344d-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6344d-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="6344d-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6344d-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="6344d-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6344d-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="6344d-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6344d-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="6344d-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-157">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6344d-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6344d-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="6344d-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-159">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="6344d-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6344d-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="6344d-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-161">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6344d-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="6344d-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6344d-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="6344d-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-164">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="6344d-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6344d-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="6344d-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-166">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="6344d-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6344d-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="6344d-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-168">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="6344d-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6344d-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="6344d-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-170">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="6344d-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6344d-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="6344d-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-172">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="6344d-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6344d-173">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6344d-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-176">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6344d-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-177">Breve descrição de um objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="6344d-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="6344d-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-179">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6344d-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-180">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6344d-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-182">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6344d-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-183">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6344d-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6344d-184">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6344d-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="6344d-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6344d-186"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="6344d-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-187">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6344d-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="6344d-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6344d-189">(1)</span><span class="sxs-lookup"><span data-stu-id="6344d-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-190">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6344d-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6344d-192">(2)</span><span class="sxs-lookup"><span data-stu-id="6344d-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6344d-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="6344d-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6344d-194">(3)</span><span class="sxs-lookup"><span data-stu-id="6344d-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-195">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="6344d-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6344d-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="6344d-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6344d-197">(4)</span><span class="sxs-lookup"><span data-stu-id="6344d-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-198">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-198">Device is not working properly.</span></span> <span data-ttu-id="6344d-199">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="6344d-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6344d-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="6344d-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6344d-201">(5)</span><span class="sxs-lookup"><span data-stu-id="6344d-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-202">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="6344d-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6344d-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="6344d-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6344d-204"> (6)</span><span class="sxs-lookup"><span data-stu-id="6344d-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-205">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6344d-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6344d-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="6344d-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6344d-207">(7)</span><span class="sxs-lookup"><span data-stu-id="6344d-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6344d-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="6344d-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6344d-209">(8)</span><span class="sxs-lookup"><span data-stu-id="6344d-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-210">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="6344d-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6344d-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="6344d-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6344d-212">(9)</span><span class="sxs-lookup"><span data-stu-id="6344d-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-213">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-213">Device is not working properly.</span></span> <span data-ttu-id="6344d-214">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6344d-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="6344d-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6344d-216">(10)</span><span class="sxs-lookup"><span data-stu-id="6344d-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-217">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6344d-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="6344d-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6344d-219">(11)</span><span class="sxs-lookup"><span data-stu-id="6344d-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-220">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6344d-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="6344d-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6344d-222">12</span><span class="sxs-lookup"><span data-stu-id="6344d-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-223">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="6344d-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6344d-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6344d-225">(13)</span><span class="sxs-lookup"><span data-stu-id="6344d-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-226">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6344d-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="6344d-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6344d-228">(14)</span><span class="sxs-lookup"><span data-stu-id="6344d-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-229">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="6344d-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6344d-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="6344d-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6344d-231">(15)</span><span class="sxs-lookup"><span data-stu-id="6344d-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-232">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="6344d-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6344d-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="6344d-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6344d-234">(16)</span><span class="sxs-lookup"><span data-stu-id="6344d-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-235">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="6344d-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6344d-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="6344d-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6344d-237">(17)</span><span class="sxs-lookup"><span data-stu-id="6344d-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-238">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6344d-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6344d-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6344d-240">(18)</span><span class="sxs-lookup"><span data-stu-id="6344d-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-241">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="6344d-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6344d-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="6344d-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6344d-243">(19)</span><span class="sxs-lookup"><span data-stu-id="6344d-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6344d-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="6344d-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6344d-245">(20)</span><span class="sxs-lookup"><span data-stu-id="6344d-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-246">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="6344d-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6344d-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6344d-248">(21)</span><span class="sxs-lookup"><span data-stu-id="6344d-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-249">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="6344d-249">System failure.</span></span> <span data-ttu-id="6344d-250">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="6344d-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6344d-251">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6344d-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="6344d-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6344d-253">(22)</span><span class="sxs-lookup"><span data-stu-id="6344d-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-254">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6344d-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6344d-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="6344d-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6344d-256">(23)</span><span class="sxs-lookup"><span data-stu-id="6344d-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-257">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="6344d-257">System failure.</span></span> <span data-ttu-id="6344d-258">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="6344d-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6344d-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="6344d-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6344d-260">(24)</span><span class="sxs-lookup"><span data-stu-id="6344d-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-261">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="6344d-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6344d-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6344d-263">(25)</span><span class="sxs-lookup"><span data-stu-id="6344d-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-264">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6344d-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6344d-266">(26)</span><span class="sxs-lookup"><span data-stu-id="6344d-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-267">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6344d-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6344d-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="6344d-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6344d-269">(27)</span><span class="sxs-lookup"><span data-stu-id="6344d-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-270">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="6344d-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6344d-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="6344d-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6344d-272">(28)</span><span class="sxs-lookup"><span data-stu-id="6344d-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-273">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="6344d-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6344d-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="6344d-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6344d-275">(29)</span><span class="sxs-lookup"><span data-stu-id="6344d-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-276">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6344d-276">Device is disabled.</span></span> <span data-ttu-id="6344d-277">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="6344d-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6344d-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="6344d-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6344d-279">(30)</span><span class="sxs-lookup"><span data-stu-id="6344d-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-280">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="6344d-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6344d-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6344d-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6344d-282">(31)</span><span class="sxs-lookup"><span data-stu-id="6344d-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-283">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-283">Device is not working properly.</span></span> <span data-ttu-id="6344d-284">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="6344d-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6344d-285">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6344d-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-286">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6344d-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-288">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6344d-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-289">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6344d-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6344d-290">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-291">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6344d-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-294">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6344d-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6344d-295">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="6344d-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6344d-296">Quando usado com as outras propriedades de chave de uma classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="6344d-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="6344d-297">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-298">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="6344d-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-299">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-301">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-302">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="6344d-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="6344d-303">As implementações atuais do WMI não preenchem a propriedade **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="6344d-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="6344d-304">A presença da propriedade **CurrentReading** é reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6344d-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="6344d-305">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-306">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6344d-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-309">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="6344d-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-310">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="6344d-310">Description of the object.</span></span>

<span data-ttu-id="6344d-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6344d-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-315">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="6344d-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-316">Identificador exclusivo da investigação atual.</span><span class="sxs-lookup"><span data-stu-id="6344d-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="6344d-317">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6344d-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-319">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6344d-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6344d-321">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="6344d-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="6344d-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6344d-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6344d-326">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que você pode tomar.</span><span class="sxs-lookup"><span data-stu-id="6344d-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="6344d-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6344d-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-329">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6344d-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-331">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="6344d-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-332">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="6344d-332">Date and time the object is installed.</span></span> <span data-ttu-id="6344d-333">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="6344d-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6344d-334">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-335">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="6344d-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-336">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6344d-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6344d-338">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6344d-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="6344d-339">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6344d-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-341">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6344d-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6344d-343">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6344d-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6344d-344">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="6344d-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-346">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-348">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,13 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-349">Valor do limite do sensor para especificar os intervalos (valores mínimos e máximos) que identificam as condições operacionais do sensor, que podem ser condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="6344d-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6344d-350">Se **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="6344d-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="6344d-351">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="6344d-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-353">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-355">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,15 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-356">Valor do limite do sensor para especificar os intervalos (valores mínimos e máximos) que identificam as condições operacionais do sensor, que podem ser condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="6344d-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6344d-357">Se **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="6344d-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="6344d-358">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="6344d-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-360">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-362">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-363">Valor do limite do sensor para especificar os intervalos (valores mínimos e máximos) que identificam as condições operacionais do sensor, que podem ser condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="6344d-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6344d-364">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="6344d-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="6344d-365">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="6344d-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="6344d-366">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="6344d-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-368">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-370">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,9 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-371">Maior valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="6344d-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="6344d-372">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="6344d-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-374">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-376">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,10 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-377">Menor valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="6344d-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="6344d-378">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-379">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6344d-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-380">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-382">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6344d-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-383">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="6344d-383">Label for the object.</span></span> <span data-ttu-id="6344d-384">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="6344d-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6344d-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="6344d-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-387">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-389">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-390">Valor normal ou esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="6344d-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="6344d-391">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="6344d-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-393">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-395">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-396">Valor normal ou esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="6344d-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="6344d-397">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="6344d-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-399">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-401">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-402">Diretrizes para o usuário para o intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="6344d-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="6344d-403">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6344d-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-405">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-407">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6344d-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-408">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6344d-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6344d-409">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6344d-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="6344d-410">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6344d-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-412">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6344d-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6344d-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6344d-414">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6344d-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6344d-415">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6344d-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6344d-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6344d-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6344d-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6344d-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="6344d-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6344d-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6344d-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-420">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6344d-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6344d-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="6344d-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-422">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="6344d-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6344d-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="6344d-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-424">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="6344d-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6344d-425">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="6344d-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6344d-426">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6344d-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="6344d-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-428">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="6344d-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6344d-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="6344d-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6344d-430">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="6344d-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6344d-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6344d-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-432">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6344d-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6344d-434">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="6344d-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="6344d-435">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="6344d-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="6344d-436">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-437">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="6344d-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-438">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6344d-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-440">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,17 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" centésimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-441">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="6344d-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="6344d-442">Esse valor pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6344d-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6344d-443">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-444">**Status**</span><span class="sxs-lookup"><span data-stu-id="6344d-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-447">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="6344d-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-448">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6344d-448">Current status of the object.</span></span> <span data-ttu-id="6344d-449">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="6344d-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6344d-450">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6344d-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6344d-451">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6344d-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6344d-452">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6344d-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6344d-453">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6344d-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6344d-454">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6344d-455">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6344d-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6344d-456">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6344d-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6344d-457">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="6344d-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6344d-458">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6344d-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6344d-459">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6344d-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6344d-460">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6344d-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6344d-461">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6344d-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6344d-462">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="6344d-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6344d-463">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="6344d-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6344d-464">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="6344d-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6344d-465">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6344d-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6344d-466">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="6344d-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6344d-467">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="6344d-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6344d-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6344d-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-469">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6344d-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-471">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="6344d-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-472">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6344d-472">State of the logical device.</span></span> <span data-ttu-id="6344d-473">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="6344d-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6344d-474">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6344d-475">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6344d-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6344d-476">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="6344d-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6344d-477">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6344d-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6344d-478">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="6344d-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6344d-479">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="6344d-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6344d-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6344d-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-481">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-483">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6344d-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6344d-484">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="6344d-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="6344d-485">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6344d-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6344d-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-489">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6344d-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6344d-490">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="6344d-490">Name of the scoping system.</span></span>

<span data-ttu-id="6344d-491">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-492">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="6344d-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-493">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-494">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-495">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,18 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-496">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="6344d-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="6344d-497">A tolerância, juntamente com a resolução e a precisão, é usada para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="6344d-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="6344d-498">A tolerância pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="6344d-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="6344d-499">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-500">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="6344d-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-501">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-502">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-503">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,14 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-504">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) que identificam as condições operacionais do sensor, que podem ser condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="6344d-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6344d-505">Se **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="6344d-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="6344d-506">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-507">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="6344d-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-508">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-510">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,16 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-511">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) que identificam as condições operacionais do sensor, que podem ser condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="6344d-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6344d-512">Se **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="6344d-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="6344d-513">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6344d-514">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="6344d-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6344d-515">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6344d-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6344d-516">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6344d-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6344d-517">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de temperatura DMTF \| 1,12 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de graus centigrade ")</span><span class="sxs-lookup"><span data-stu-id="6344d-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="6344d-518">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) que identificam as condições operacionais do sensor, que podem ser condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="6344d-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="6344d-519">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="6344d-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="6344d-520">Se **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="6344d-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="6344d-521">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6344d-522">Comentários</span><span class="sxs-lookup"><span data-stu-id="6344d-522">Remarks</span></span>

<span data-ttu-id="6344d-523">A classe **Win32 \_ TemperatureProbe** é derivada de [**CIM \_ sensor**](cim-temperaturesensor.md).</span><span class="sxs-lookup"><span data-stu-id="6344d-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6344d-524">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6344d-524">Examples</span></span>

<span data-ttu-id="6344d-525">O exemplo a seguir retorna dados de investigação de temperatura para o computador local.</span><span class="sxs-lookup"><span data-stu-id="6344d-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="6344d-526">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6344d-526">Requirements</span></span>



| <span data-ttu-id="6344d-527">Requisito</span><span class="sxs-lookup"><span data-stu-id="6344d-527">Requirement</span></span> | <span data-ttu-id="6344d-528">Valor</span><span class="sxs-lookup"><span data-stu-id="6344d-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6344d-529">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6344d-529">Minimum supported client</span></span><br/> | <span data-ttu-id="6344d-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6344d-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6344d-531">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6344d-531">Minimum supported server</span></span><br/> | <span data-ttu-id="6344d-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6344d-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6344d-533">Namespace</span><span class="sxs-lookup"><span data-stu-id="6344d-533">Namespace</span></span><br/>                | <span data-ttu-id="6344d-534">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6344d-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6344d-535">MOF</span><span class="sxs-lookup"><span data-stu-id="6344d-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6344d-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6344d-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6344d-537">DLL</span><span class="sxs-lookup"><span data-stu-id="6344d-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6344d-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6344d-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6344d-539">Confira também</span><span class="sxs-lookup"><span data-stu-id="6344d-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6344d-540">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="6344d-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="6344d-541">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="6344d-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
