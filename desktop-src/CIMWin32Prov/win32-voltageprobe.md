---
description: A \_ classe WMI VoltageProbe do Win32 representa as propriedades de um sensor de tensão (voltímetro eletrônico).
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Classe Win32_VoltageProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163924"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="a217b-103">\_Classe Win32 VoltageProbe</span><span class="sxs-lookup"><span data-stu-id="a217b-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="a217b-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VoltageProbe do Win32** representa as propriedades de um sensor de tensão (voltímetro eletrônico).</span><span class="sxs-lookup"><span data-stu-id="a217b-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="a217b-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a217b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a217b-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a217b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a217b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a217b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="a217b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a217b-108">Members</span></span>

<span data-ttu-id="a217b-109">A classe **Win32 \_ VoltageProbe** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a217b-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="a217b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a217b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a217b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a217b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a217b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a217b-112">Methods</span></span>

<span data-ttu-id="a217b-113">A classe **Win32 \_ VoltageProbe** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a217b-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="a217b-114">Método</span><span class="sxs-lookup"><span data-stu-id="a217b-114">Method</span></span>            | <span data-ttu-id="a217b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a217b-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a217b-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a217b-116">**Reset**</span></span>         | <span data-ttu-id="a217b-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a217b-117">Not implemented.</span></span> <span data-ttu-id="a217b-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ voltagem**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="a217b-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a217b-119">**SetPowerState**</span></span> | <span data-ttu-id="a217b-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a217b-120">Not implemented.</span></span> <span data-ttu-id="a217b-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ voltagem**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a217b-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a217b-122">Properties</span></span>

<span data-ttu-id="a217b-123">A classe **Win32 \_ VoltageProbe** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a217b-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a217b-124">**Correta**</span><span class="sxs-lookup"><span data-stu-id="a217b-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-125">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-127">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,19 ")</span><span class="sxs-lookup"><span data-stu-id="a217b-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-128">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="a217b-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="a217b-129">O valor de precisão é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="a217b-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="a217b-130">A precisão, juntamente com a resolução e a tolerância, é usada para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="a217b-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="a217b-131">A precisão pode variar e depende se o dispositivo é linear ou não em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="a217b-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="a217b-132">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-133">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="a217b-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a217b-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-136">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a217b-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-137">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-137">Availability and status of the device.</span></span>

<span data-ttu-id="a217b-138">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a217b-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a217b-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a217b-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a217b-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a217b-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a217b-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a217b-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="a217b-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a217b-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="a217b-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a217b-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="a217b-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a217b-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="a217b-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a217b-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="a217b-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a217b-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="a217b-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a217b-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a217b-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a217b-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a217b-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a217b-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="a217b-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a217b-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="a217b-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-152">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a217b-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a217b-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="a217b-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-154">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="a217b-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a217b-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a217b-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-156">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a217b-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="a217b-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a217b-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="a217b-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-159">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="a217b-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a217b-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a217b-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-161">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="a217b-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a217b-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="a217b-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-163">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="a217b-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a217b-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a217b-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-165">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="a217b-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a217b-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="a217b-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-167">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="a217b-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a217b-168">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a217b-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-171">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a217b-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-172">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="a217b-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="a217b-173">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a217b-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-175">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a217b-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-177">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a217b-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-178">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a217b-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a217b-179">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a217b-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a217b-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a217b-181"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="a217b-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-182">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a217b-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="a217b-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a217b-184">(1)</span><span class="sxs-lookup"><span data-stu-id="a217b-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-185">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a217b-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a217b-187">(2)</span><span class="sxs-lookup"><span data-stu-id="a217b-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a217b-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a217b-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a217b-189">(3)</span><span class="sxs-lookup"><span data-stu-id="a217b-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-190">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="a217b-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a217b-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a217b-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a217b-192">(4)</span><span class="sxs-lookup"><span data-stu-id="a217b-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-193">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-193">Device is not working properly.</span></span> <span data-ttu-id="a217b-194">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a217b-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a217b-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="a217b-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a217b-196">(5)</span><span class="sxs-lookup"><span data-stu-id="a217b-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-197">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="a217b-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a217b-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a217b-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a217b-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="a217b-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-200">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a217b-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a217b-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a217b-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a217b-202">(7)</span><span class="sxs-lookup"><span data-stu-id="a217b-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a217b-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="a217b-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a217b-204">(8)</span><span class="sxs-lookup"><span data-stu-id="a217b-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-205">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="a217b-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a217b-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="a217b-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a217b-207">(9)</span><span class="sxs-lookup"><span data-stu-id="a217b-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-208">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-208">Device is not working properly.</span></span> <span data-ttu-id="a217b-209">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a217b-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="a217b-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a217b-211">(10)</span><span class="sxs-lookup"><span data-stu-id="a217b-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-212">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a217b-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="a217b-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a217b-214">(11)</span><span class="sxs-lookup"><span data-stu-id="a217b-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-215">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a217b-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="a217b-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a217b-217">12</span><span class="sxs-lookup"><span data-stu-id="a217b-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-218">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="a217b-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a217b-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a217b-220">(13)</span><span class="sxs-lookup"><span data-stu-id="a217b-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-221">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a217b-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="a217b-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a217b-223">(14)</span><span class="sxs-lookup"><span data-stu-id="a217b-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-224">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="a217b-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a217b-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="a217b-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a217b-226">(15)</span><span class="sxs-lookup"><span data-stu-id="a217b-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-227">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="a217b-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a217b-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="a217b-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a217b-229">(16)</span><span class="sxs-lookup"><span data-stu-id="a217b-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-230">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="a217b-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a217b-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="a217b-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a217b-232">(17)</span><span class="sxs-lookup"><span data-stu-id="a217b-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-233">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a217b-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a217b-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a217b-235">(18)</span><span class="sxs-lookup"><span data-stu-id="a217b-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-236">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="a217b-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a217b-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="a217b-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a217b-238">(19)</span><span class="sxs-lookup"><span data-stu-id="a217b-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a217b-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="a217b-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a217b-240">(20)</span><span class="sxs-lookup"><span data-stu-id="a217b-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-241">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="a217b-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a217b-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a217b-243">(21)</span><span class="sxs-lookup"><span data-stu-id="a217b-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a217b-244">System failure.</span></span> <span data-ttu-id="a217b-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a217b-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a217b-246">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a217b-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a217b-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a217b-248">(22)</span><span class="sxs-lookup"><span data-stu-id="a217b-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-249">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a217b-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a217b-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="a217b-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a217b-251">(23)</span><span class="sxs-lookup"><span data-stu-id="a217b-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-252">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="a217b-252">System failure.</span></span> <span data-ttu-id="a217b-253">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="a217b-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a217b-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="a217b-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a217b-255">(24)</span><span class="sxs-lookup"><span data-stu-id="a217b-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-256">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="a217b-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a217b-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a217b-258">(25)</span><span class="sxs-lookup"><span data-stu-id="a217b-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a217b-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a217b-261">(26)</span><span class="sxs-lookup"><span data-stu-id="a217b-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-262">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a217b-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a217b-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="a217b-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a217b-264">(27)</span><span class="sxs-lookup"><span data-stu-id="a217b-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-265">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="a217b-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a217b-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="a217b-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a217b-267">(28)</span><span class="sxs-lookup"><span data-stu-id="a217b-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-268">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="a217b-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a217b-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="a217b-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a217b-270">(29)</span><span class="sxs-lookup"><span data-stu-id="a217b-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-271">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a217b-271">Device is disabled.</span></span> <span data-ttu-id="a217b-272">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="a217b-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a217b-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a217b-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a217b-274">(30)</span><span class="sxs-lookup"><span data-stu-id="a217b-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-275">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a217b-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a217b-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a217b-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a217b-277">(31)</span><span class="sxs-lookup"><span data-stu-id="a217b-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-278">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-278">Device is not working properly.</span></span> <span data-ttu-id="a217b-279">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="a217b-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a217b-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a217b-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-281">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a217b-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-283">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a217b-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-284">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a217b-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a217b-285">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a217b-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-289">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a217b-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a217b-290">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a217b-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a217b-291">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a217b-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a217b-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-293">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="a217b-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-294">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-296">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-297">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="a217b-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="a217b-298">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-299">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a217b-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-302">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a217b-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-303">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a217b-303">Description of the object.</span></span>

<span data-ttu-id="a217b-304">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a217b-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-308">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a217b-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-309">Identificador exclusivo da investigação de tensão.</span><span class="sxs-lookup"><span data-stu-id="a217b-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="a217b-310">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a217b-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a217b-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a217b-314">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="a217b-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a217b-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a217b-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a217b-319">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="a217b-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="a217b-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a217b-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-322">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a217b-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-324">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a217b-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-325">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a217b-325">Date and time the object is installed.</span></span> <span data-ttu-id="a217b-326">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a217b-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a217b-327">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-328">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="a217b-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-329">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a217b-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a217b-331">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="a217b-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="a217b-332">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-333">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a217b-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-334">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a217b-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a217b-336">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a217b-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a217b-337">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-338">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="a217b-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-339">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-341">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,13 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-342">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="a217b-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="a217b-343">Se **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="a217b-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="a217b-344">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-345">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="a217b-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-346">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-348">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,15 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-349">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="a217b-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="a217b-350">Se **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="a217b-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="a217b-351">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-352">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="a217b-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-353">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-355">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-356">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="a217b-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="a217b-357">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="a217b-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="a217b-358">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="a217b-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="a217b-359">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-360">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="a217b-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-361">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-363">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,9 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-364">Maior valor da propriedade medida que o sensor numérico pode ler.</span><span class="sxs-lookup"><span data-stu-id="a217b-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="a217b-365">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-366">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="a217b-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-367">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-369">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,10 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-370">Menor valor da propriedade medida que o sensor numérico pode ler.</span><span class="sxs-lookup"><span data-stu-id="a217b-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="a217b-371">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-372">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a217b-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-375">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a217b-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-376">Rótulo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a217b-376">Label for an object.</span></span> <span data-ttu-id="a217b-377">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="a217b-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a217b-378">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-379">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="a217b-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-380">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-382">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-383">Valor normal ou esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="a217b-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="a217b-384">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-385">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="a217b-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-386">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-388">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-389">Valor normal ou esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="a217b-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="a217b-390">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-391">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="a217b-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-392">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-394">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-395">Orientação para o usuário indicar o intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="a217b-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="a217b-396">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a217b-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-400">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a217b-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-401">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a217b-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a217b-402">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a217b-403">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a217b-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a217b-404">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a217b-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-405">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a217b-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a217b-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a217b-407">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a217b-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a217b-408">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="a217b-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a217b-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a217b-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a217b-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="a217b-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a217b-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a217b-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a217b-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a217b-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-413">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a217b-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a217b-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a217b-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-415">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="a217b-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a217b-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="a217b-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-417">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="a217b-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a217b-418">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="a217b-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a217b-419">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a217b-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="a217b-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-421">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="a217b-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a217b-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="a217b-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a217b-423">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="a217b-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a217b-424">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a217b-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-425">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a217b-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a217b-427">Se **for true**, o dispositivo poderá ser gerenciado por energia, o que significa que ele pode ser colocado no modo de suspensão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a217b-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="a217b-428">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, mas indica que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="a217b-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="a217b-429">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-430">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="a217b-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-431">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a217b-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-433">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,17 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimos de milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-434">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="a217b-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="a217b-435">Esse valor pode variar e depende se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="a217b-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="a217b-436">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-437">**Status**</span><span class="sxs-lookup"><span data-stu-id="a217b-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-438">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-440">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a217b-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-441">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a217b-441">Current status of the object.</span></span> <span data-ttu-id="a217b-442">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="a217b-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a217b-443">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a217b-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a217b-444">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="a217b-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a217b-445">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="a217b-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a217b-446">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="a217b-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a217b-447">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a217b-448">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a217b-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a217b-449">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a217b-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a217b-450">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a217b-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a217b-451">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a217b-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a217b-452">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a217b-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a217b-453">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a217b-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a217b-454">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a217b-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a217b-455">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a217b-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a217b-456">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a217b-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a217b-457">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a217b-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a217b-458">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a217b-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a217b-459">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a217b-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a217b-460">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a217b-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a217b-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a217b-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-462">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a217b-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-464">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="a217b-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-465">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a217b-465">State of the logical device.</span></span> <span data-ttu-id="a217b-466">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="a217b-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a217b-467">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a217b-468">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a217b-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a217b-469">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="a217b-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a217b-470">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a217b-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a217b-471">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a217b-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a217b-472">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="a217b-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a217b-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a217b-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-476">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a217b-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a217b-477">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="a217b-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="a217b-478">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a217b-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-480">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a217b-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-482">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a217b-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a217b-483">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a217b-483">Name of the scoping system.</span></span>

<span data-ttu-id="a217b-484">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-485">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="a217b-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-486">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-488">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,18 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-489">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="a217b-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="a217b-490">A tolerância, juntamente com a resolução e a precisão, é usada para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="a217b-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="a217b-491">A tolerância pode variar e depende se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="a217b-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="a217b-492">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-493">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="a217b-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-494">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-496">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,14 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-497">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="a217b-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="a217b-498">Se **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="a217b-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="a217b-499">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-500">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="a217b-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-501">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-502">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-503">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,16 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-504">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="a217b-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="a217b-505">Se **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="a217b-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="a217b-506">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="a217b-507">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="a217b-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a217b-508">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a217b-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a217b-509">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a217b-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a217b-510">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Investigação de tensão DMTF \| 1,12 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="a217b-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a217b-511">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="a217b-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="a217b-512">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="a217b-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="a217b-513">Se **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="a217b-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="a217b-514">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a217b-515">Comentários</span><span class="sxs-lookup"><span data-stu-id="a217b-515">Remarks</span></span>

<span data-ttu-id="a217b-516">A classe **Win32 \_ VoltageProbe** é derivada de [**CIM \_ voltagem**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="a217b-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a217b-517">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a217b-517">Requirements</span></span>



| <span data-ttu-id="a217b-518">Requisito</span><span class="sxs-lookup"><span data-stu-id="a217b-518">Requirement</span></span> | <span data-ttu-id="a217b-519">Valor</span><span class="sxs-lookup"><span data-stu-id="a217b-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a217b-520">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a217b-520">Minimum supported client</span></span><br/> | <span data-ttu-id="a217b-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a217b-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a217b-522">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a217b-522">Minimum supported server</span></span><br/> | <span data-ttu-id="a217b-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a217b-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a217b-524">Namespace</span><span class="sxs-lookup"><span data-stu-id="a217b-524">Namespace</span></span><br/>                | <span data-ttu-id="a217b-525">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a217b-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a217b-526">MOF</span><span class="sxs-lookup"><span data-stu-id="a217b-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a217b-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a217b-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a217b-528">DLL</span><span class="sxs-lookup"><span data-stu-id="a217b-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a217b-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a217b-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a217b-530">Confira também</span><span class="sxs-lookup"><span data-stu-id="a217b-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a217b-531">**\_Voltagem CIM**</span><span class="sxs-lookup"><span data-stu-id="a217b-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="a217b-532">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="a217b-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
