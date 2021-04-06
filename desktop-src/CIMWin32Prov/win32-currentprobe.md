---
description: A \_ classe WMI CurrentProbe do Win32 representa as propriedades de um ammeter (sensor de monitoramento atual).
ms.assetid: 2e1da856-b787-404b-ac4b-080c4950bad8
ms.tgt_platform: multiple
title: Classe Win32_CurrentProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CurrentProbe
- Win32_CurrentProbe.Reset
- Win32_CurrentProbe.SetPowerState
- Win32_CurrentProbe.Accuracy
- Win32_CurrentProbe.Availability
- Win32_CurrentProbe.Caption
- Win32_CurrentProbe.ConfigManagerErrorCode
- Win32_CurrentProbe.ConfigManagerUserConfig
- Win32_CurrentProbe.CreationClassName
- Win32_CurrentProbe.CurrentReading
- Win32_CurrentProbe.Description
- Win32_CurrentProbe.DeviceID
- Win32_CurrentProbe.ErrorCleared
- Win32_CurrentProbe.ErrorDescription
- Win32_CurrentProbe.InstallDate
- Win32_CurrentProbe.IsLinear
- Win32_CurrentProbe.LastErrorCode
- Win32_CurrentProbe.LowerThresholdCritical
- Win32_CurrentProbe.LowerThresholdFatal
- Win32_CurrentProbe.LowerThresholdNonCritical
- Win32_CurrentProbe.MaxReadable
- Win32_CurrentProbe.MinReadable
- Win32_CurrentProbe.Name
- Win32_CurrentProbe.NominalReading
- Win32_CurrentProbe.NormalMax
- Win32_CurrentProbe.NormalMin
- Win32_CurrentProbe.PNPDeviceID
- Win32_CurrentProbe.PowerManagementCapabilities
- Win32_CurrentProbe.PowerManagementSupported
- Win32_CurrentProbe.Resolution
- Win32_CurrentProbe.Status
- Win32_CurrentProbe.StatusInfo
- Win32_CurrentProbe.SystemCreationClassName
- Win32_CurrentProbe.SystemName
- Win32_CurrentProbe.Tolerance
- Win32_CurrentProbe.UpperThresholdCritical
- Win32_CurrentProbe.UpperThresholdFatal
- Win32_CurrentProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be834e56eb3d958a8cd6ee653dc9a248c14ae3bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826690"
---
# <a name="win32_currentprobe-class"></a><span data-ttu-id="67584-103">\_Classe Win32 CurrentProbe</span><span class="sxs-lookup"><span data-stu-id="67584-103">Win32\_CurrentProbe class</span></span>

<span data-ttu-id="67584-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CurrentProbe do Win32** representa as propriedades de um ammeter (sensor de monitoramento atual).</span><span class="sxs-lookup"><span data-stu-id="67584-104">The **Win32\_CurrentProbe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a current monitoring sensor (ammeter).</span></span>

<span data-ttu-id="67584-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="67584-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="67584-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="67584-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67584-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67584-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABA-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_CurrentProbe : CIM_CurrentSensor
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

## <a name="members"></a><span data-ttu-id="67584-108">Membros</span><span class="sxs-lookup"><span data-stu-id="67584-108">Members</span></span>

<span data-ttu-id="67584-109">A classe **Win32 \_ CurrentProbe** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="67584-109">The **Win32\_CurrentProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="67584-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="67584-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="67584-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67584-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="67584-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="67584-112">Methods</span></span>

<span data-ttu-id="67584-113">A classe **Win32 \_ CurrentProbe** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="67584-113">The **Win32\_CurrentProbe** class has these methods.</span></span>



| <span data-ttu-id="67584-114">Método</span><span class="sxs-lookup"><span data-stu-id="67584-114">Method</span></span>            | <span data-ttu-id="67584-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="67584-115">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67584-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="67584-116">**Reset**</span></span>         | <span data-ttu-id="67584-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="67584-117">Not implemented.</span></span> <span data-ttu-id="67584-118">Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ CurrentSensor**](cim-currentsensor.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="67584-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="67584-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="67584-119">**SetPowerState**</span></span> | <span data-ttu-id="67584-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="67584-120">Not implemented.</span></span> <span data-ttu-id="67584-121">Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ CurrentSensor**](cim-currentsensor.md) para obter a documentação.</span><span class="sxs-lookup"><span data-stu-id="67584-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="67584-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67584-122">Properties</span></span>

<span data-ttu-id="67584-123">A classe **Win32 \_ CurrentProbe** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="67584-123">The **Win32\_CurrentProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67584-124">**Correta**</span><span class="sxs-lookup"><span data-stu-id="67584-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-125">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-127">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,19 ")</span><span class="sxs-lookup"><span data-stu-id="67584-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="67584-128">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="67584-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="67584-129">O valor é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="67584-129">The value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="67584-130">A precisão, juntamente com a resolução e a tolerância, é usada para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="67584-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="67584-131">A precisão pode variar e depende se o dispositivo é linear ou não por seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67584-131">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="67584-132">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-133">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="67584-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-134">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67584-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67584-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-136">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="67584-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="67584-137">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-137">Availability and status of the device.</span></span>

<span data-ttu-id="67584-138">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67584-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="67584-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67584-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="67584-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="67584-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="67584-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67584-142">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="67584-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="67584-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="67584-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="67584-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="67584-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="67584-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="67584-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="67584-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="67584-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="67584-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="67584-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="67584-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="67584-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67584-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="67584-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="67584-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="67584-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="67584-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="67584-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="67584-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="67584-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="67584-153">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="67584-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="67584-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="67584-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="67584-155">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="67584-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="67584-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="67584-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="67584-157">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="67584-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="67584-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="67584-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="67584-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="67584-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="67584-160">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="67584-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="67584-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="67584-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="67584-162">Em pausa.</span><span class="sxs-lookup"><span data-stu-id="67584-162">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="67584-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="67584-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="67584-164">Não está pronto.</span><span class="sxs-lookup"><span data-stu-id="67584-164">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="67584-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="67584-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="67584-166">Não configurado.</span><span class="sxs-lookup"><span data-stu-id="67584-166">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="67584-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="67584-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="67584-168">O sensor atual não está disponível.</span><span class="sxs-lookup"><span data-stu-id="67584-168">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67584-169">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="67584-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="67584-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="67584-173">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="67584-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="67584-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67584-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="67584-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67584-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-178">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67584-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67584-179">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="67584-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="67584-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="67584-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="67584-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="67584-182"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="67584-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="67584-183">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="67584-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="67584-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="67584-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="67584-185">(1)</span><span class="sxs-lookup"><span data-stu-id="67584-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="67584-186">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="67584-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="67584-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="67584-188">(2)</span><span class="sxs-lookup"><span data-stu-id="67584-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="67584-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="67584-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="67584-190">(3)</span><span class="sxs-lookup"><span data-stu-id="67584-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="67584-191">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="67584-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="67584-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="67584-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="67584-193">(4)</span><span class="sxs-lookup"><span data-stu-id="67584-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="67584-194">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="67584-194">Device is not working properly.</span></span> <span data-ttu-id="67584-195">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="67584-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="67584-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="67584-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="67584-197">(5)</span><span class="sxs-lookup"><span data-stu-id="67584-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="67584-198">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="67584-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="67584-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="67584-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="67584-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="67584-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="67584-201">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="67584-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="67584-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="67584-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="67584-203">(7)</span><span class="sxs-lookup"><span data-stu-id="67584-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="67584-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="67584-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="67584-205">(8)</span><span class="sxs-lookup"><span data-stu-id="67584-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="67584-206">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="67584-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="67584-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="67584-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="67584-208">(9)</span><span class="sxs-lookup"><span data-stu-id="67584-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="67584-209">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="67584-209">Device is not working properly.</span></span> <span data-ttu-id="67584-210">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="67584-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="67584-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="67584-212">(10)</span><span class="sxs-lookup"><span data-stu-id="67584-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="67584-213">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="67584-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="67584-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="67584-215">(11)</span><span class="sxs-lookup"><span data-stu-id="67584-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="67584-216">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="67584-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="67584-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="67584-218">12</span><span class="sxs-lookup"><span data-stu-id="67584-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="67584-219">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="67584-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="67584-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="67584-221">(13)</span><span class="sxs-lookup"><span data-stu-id="67584-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="67584-222">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="67584-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="67584-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="67584-224">(14)</span><span class="sxs-lookup"><span data-stu-id="67584-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="67584-225">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="67584-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="67584-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="67584-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="67584-227">(15)</span><span class="sxs-lookup"><span data-stu-id="67584-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="67584-228">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="67584-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="67584-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="67584-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="67584-230">(16)</span><span class="sxs-lookup"><span data-stu-id="67584-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="67584-231">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="67584-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="67584-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="67584-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="67584-233">(17)</span><span class="sxs-lookup"><span data-stu-id="67584-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="67584-234">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="67584-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="67584-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="67584-236">(18)</span><span class="sxs-lookup"><span data-stu-id="67584-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="67584-237">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="67584-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="67584-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="67584-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="67584-239">(19)</span><span class="sxs-lookup"><span data-stu-id="67584-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="67584-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="67584-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="67584-241">(20)</span><span class="sxs-lookup"><span data-stu-id="67584-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="67584-242">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="67584-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="67584-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="67584-244">(21)</span><span class="sxs-lookup"><span data-stu-id="67584-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="67584-245">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="67584-245">System failure.</span></span> <span data-ttu-id="67584-246">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="67584-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="67584-247">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="67584-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="67584-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="67584-249">(22)</span><span class="sxs-lookup"><span data-stu-id="67584-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="67584-250">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="67584-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="67584-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="67584-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="67584-252">(23)</span><span class="sxs-lookup"><span data-stu-id="67584-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="67584-253">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="67584-253">System failure.</span></span> <span data-ttu-id="67584-254">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="67584-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="67584-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="67584-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="67584-256">(24)</span><span class="sxs-lookup"><span data-stu-id="67584-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="67584-257">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="67584-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="67584-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="67584-259">(25)</span><span class="sxs-lookup"><span data-stu-id="67584-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="67584-260">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="67584-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="67584-262">(26)</span><span class="sxs-lookup"><span data-stu-id="67584-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="67584-263">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67584-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="67584-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="67584-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="67584-265">(27)</span><span class="sxs-lookup"><span data-stu-id="67584-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="67584-266">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="67584-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="67584-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="67584-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="67584-268">(28)</span><span class="sxs-lookup"><span data-stu-id="67584-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="67584-269">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="67584-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="67584-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="67584-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="67584-271">(29)</span><span class="sxs-lookup"><span data-stu-id="67584-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="67584-272">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="67584-272">Device is disabled.</span></span> <span data-ttu-id="67584-273">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="67584-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="67584-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="67584-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="67584-275">(30)</span><span class="sxs-lookup"><span data-stu-id="67584-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="67584-276">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="67584-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="67584-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="67584-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="67584-278">(31)</span><span class="sxs-lookup"><span data-stu-id="67584-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="67584-279">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="67584-279">Device is not working properly.</span></span> <span data-ttu-id="67584-280">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="67584-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67584-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="67584-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-282">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67584-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67584-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-284">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67584-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67584-285">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="67584-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="67584-286">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67584-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-290">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67584-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67584-291">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="67584-291">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="67584-292">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="67584-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="67584-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="67584-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-295">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-295">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-297">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-297">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-298">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="67584-298">Current value indicated by the sensor.</span></span>

<span data-ttu-id="67584-299">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-299">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-300">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="67584-300">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-303">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="67584-303">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="67584-304">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="67584-304">Description of the object.</span></span>

<span data-ttu-id="67584-305">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67584-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-306">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="67584-306">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-309">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="67584-309">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="67584-310">Identificador exclusivo da investigação atual.</span><span class="sxs-lookup"><span data-stu-id="67584-310">Unique identifier of the current probe.</span></span>

<span data-ttu-id="67584-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-312">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="67584-312">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-313">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67584-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67584-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67584-315">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="67584-315">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="67584-316">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-317">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="67584-317">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67584-320">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="67584-320">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="67584-321">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="67584-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-323">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67584-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67584-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-325">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="67584-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="67584-326">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="67584-326">Date and time the object was installed.</span></span> <span data-ttu-id="67584-327">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="67584-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="67584-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67584-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-329">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="67584-329">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-330">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67584-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67584-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67584-332">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67584-332">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="67584-333">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-333">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="67584-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67584-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67584-337">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="67584-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="67584-338">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-339">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="67584-339">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-340">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-342">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-342">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-343">Os valores de limite de sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="67584-343">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether or not the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="67584-344">Se **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="67584-344">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="67584-345">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-345">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-346">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="67584-346">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-347">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-347">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-349">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-350">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="67584-350">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="67584-351">Se **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="67584-351">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="67584-352">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-352">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-353">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="67584-353">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-354">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-354">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-356">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-357">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="67584-357">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="67584-358">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="67584-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="67584-359">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="67584-359">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="67584-360">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-360">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-361">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="67584-361">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-362">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-362">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-364">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-365">Maior valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="67584-365">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="67584-366">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-367">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="67584-367">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-368">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-370">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-371">Menor valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="67584-371">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="67584-372">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-373">**Nome**</span><span class="sxs-lookup"><span data-stu-id="67584-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-374">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-376">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="67584-376">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="67584-377">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="67584-377">Label by which the object is known.</span></span> <span data-ttu-id="67584-378">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="67584-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="67584-379">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67584-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-380">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="67584-380">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-381">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-381">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-383">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-384">Valor normal ou esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="67584-384">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="67584-385">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-385">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-386">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="67584-386">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-387">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-389">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-390">Valor normal ou esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="67584-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="67584-391">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-392">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="67584-392">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-393">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-395">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-396">Diretrizes para o usuário para o intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="67584-396">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="67584-397">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-398">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="67584-398">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-401">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67584-401">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67584-402">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="67584-402">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="67584-403">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="67584-404">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="67584-404">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="67584-405">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="67584-405">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-406">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67584-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67584-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67584-408">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="67584-408">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="67584-409">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="67584-409">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67584-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="67584-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="67584-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="67584-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67584-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="67584-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67584-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="67584-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67584-414">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="67584-414">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="67584-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="67584-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="67584-416">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="67584-416">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="67584-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="67584-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="67584-418">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="67584-418">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="67584-419">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="67584-419">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="67584-420">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="67584-420">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="67584-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="67584-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="67584-422">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="67584-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="67584-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="67584-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="67584-424">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="67584-424">Timed Power-On Supported</span></span>

<span data-ttu-id="67584-425">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="67584-425">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67584-426">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="67584-426">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-427">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="67584-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67584-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67584-429">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="67584-429">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="67584-430">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="67584-430">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="67584-431">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-432">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="67584-432">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-433">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67584-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-435">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimos de milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-436">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="67584-436">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="67584-437">Esse valor pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67584-437">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="67584-438">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-438">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-439">**Status**</span><span class="sxs-lookup"><span data-stu-id="67584-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-442">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="67584-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="67584-443">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="67584-443">Current status of the object.</span></span> <span data-ttu-id="67584-444">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="67584-444">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="67584-445">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="67584-445">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="67584-446">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="67584-446">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="67584-447">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="67584-447">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="67584-448">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="67584-448">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="67584-449">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67584-449">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="67584-450">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="67584-450">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="67584-451">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="67584-451">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="67584-452">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="67584-452">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67584-453">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="67584-453">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67584-454">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="67584-454">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="67584-455">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="67584-455">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="67584-456">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="67584-456">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="67584-457">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="67584-457">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="67584-458">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="67584-458">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="67584-459">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="67584-459">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="67584-460">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="67584-460">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="67584-461">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="67584-461">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="67584-462">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="67584-462">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67584-463">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="67584-463">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-464">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67584-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67584-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-466">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="67584-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="67584-467">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="67584-467">State of the logical device.</span></span> <span data-ttu-id="67584-468">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="67584-468">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="67584-469">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67584-470">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="67584-470">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67584-471">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="67584-471">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67584-472">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="67584-472">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67584-473">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="67584-473">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="67584-474">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="67584-474">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67584-475">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67584-475">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-476">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-478">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67584-478">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67584-479">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="67584-479">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="67584-480">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-481">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="67584-481">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-482">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67584-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67584-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-484">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67584-484">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67584-485">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="67584-485">Name of the scoping system.</span></span>

<span data-ttu-id="67584-486">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="67584-486">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-487">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="67584-487">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-488">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-488">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-489">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-490">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-490">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-491">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="67584-491">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="67584-492">A tolerância, juntamente com a resolução e a precisão, é usada para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="67584-492">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="67584-493">A tolerância pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67584-493">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="67584-494">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-494">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-495">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="67584-495">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-496">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-496">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-497">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-498">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-499">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="67584-499">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="67584-500">Se **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="67584-500">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="67584-501">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-501">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-502">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="67584-502">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-503">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-503">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-504">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-505">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-506">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="67584-506">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="67584-507">Se **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="67584-507">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="67584-508">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-508">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67584-509">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="67584-509">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67584-510">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67584-510">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67584-511">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67584-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67584-512">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="67584-512">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="67584-513">Os valores de limite do sensor especificam os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="67584-513">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="67584-514">Se **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="67584-514">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="67584-515">Se **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="67584-515">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="67584-516">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-516">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67584-517">Comentários</span><span class="sxs-lookup"><span data-stu-id="67584-517">Remarks</span></span>

<span data-ttu-id="67584-518">A classe **Win32 \_ CurrentProbe** é derivada de [**CIM \_ CurrentSensor**](cim-currentsensor.md).</span><span class="sxs-lookup"><span data-stu-id="67584-518">The **Win32\_CurrentProbe** class is derived from [**CIM\_CurrentSensor**](cim-currentsensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67584-519">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67584-519">Requirements</span></span>



| <span data-ttu-id="67584-520">Requisito</span><span class="sxs-lookup"><span data-stu-id="67584-520">Requirement</span></span> | <span data-ttu-id="67584-521">Valor</span><span class="sxs-lookup"><span data-stu-id="67584-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67584-522">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67584-522">Minimum supported client</span></span><br/> | <span data-ttu-id="67584-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67584-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67584-524">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67584-524">Minimum supported server</span></span><br/> | <span data-ttu-id="67584-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67584-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67584-526">Namespace</span><span class="sxs-lookup"><span data-stu-id="67584-526">Namespace</span></span><br/>                | <span data-ttu-id="67584-527">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="67584-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67584-528">MOF</span><span class="sxs-lookup"><span data-stu-id="67584-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67584-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67584-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67584-530">DLL</span><span class="sxs-lookup"><span data-stu-id="67584-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67584-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67584-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67584-532">Confira também</span><span class="sxs-lookup"><span data-stu-id="67584-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67584-533">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="67584-533">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="67584-534">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="67584-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

