---
description: A \_ classe CIM voltagem existe para compatibilidade com versões anteriores de definições de esquema CIM. Com adições às classes do \_ sensor CIM e \_ do CIM NumericSensor na versão 2,2, ela não é mais necessária.
ms.assetid: a578c7a2-27d5-4bd8-86d7-3962d5091f14
ms.tgt_platform: multiple
title: Classe CIM_VoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor
- CIM_VoltageSensor.Accuracy
- CIM_VoltageSensor.Availability
- CIM_VoltageSensor.Caption
- CIM_VoltageSensor.ConfigManagerErrorCode
- CIM_VoltageSensor.ConfigManagerUserConfig
- CIM_VoltageSensor.CreationClassName
- CIM_VoltageSensor.CurrentReading
- CIM_VoltageSensor.Description
- CIM_VoltageSensor.DeviceID
- CIM_VoltageSensor.ErrorCleared
- CIM_VoltageSensor.ErrorDescription
- CIM_VoltageSensor.InstallDate
- CIM_VoltageSensor.IsLinear
- CIM_VoltageSensor.LastErrorCode
- CIM_VoltageSensor.LowerThresholdCritical
- CIM_VoltageSensor.LowerThresholdFatal
- CIM_VoltageSensor.LowerThresholdNonCritical
- CIM_VoltageSensor.MaxReadable
- CIM_VoltageSensor.MinReadable
- CIM_VoltageSensor.Name
- CIM_VoltageSensor.NominalReading
- CIM_VoltageSensor.NormalMax
- CIM_VoltageSensor.NormalMin
- CIM_VoltageSensor.PNPDeviceID
- CIM_VoltageSensor.PowerManagementCapabilities
- CIM_VoltageSensor.PowerManagementSupported
- CIM_VoltageSensor.Resolution
- CIM_VoltageSensor.Status
- CIM_VoltageSensor.StatusInfo
- CIM_VoltageSensor.SystemCreationClassName
- CIM_VoltageSensor.SystemName
- CIM_VoltageSensor.Tolerance
- CIM_VoltageSensor.UpperThresholdCritical
- CIM_VoltageSensor.UpperThresholdFatal
- CIM_VoltageSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bd0f3d79415254d0af50429c8f1776d2eb451cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755666"
---
# <a name="cim_voltagesensor-class"></a><span data-ttu-id="3d24a-104">\_Classe CIM voltagem</span><span class="sxs-lookup"><span data-stu-id="3d24a-104">CIM\_VoltageSensor class</span></span>

<span data-ttu-id="3d24a-105">A classe **CIM \_ voltagem** existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="3d24a-105">The **CIM\_VoltageSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="3d24a-106">Com adições às classes [**do \_ sensor CIM**](cim-sensor.md) e do [**cim \_ NumericSensor**](cim-numericsensor.md) na versão 2,2, ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="3d24a-106">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="3d24a-107">Um sensor de tensão pode ser definido definindo a propriedade **SensorType** , herdada [**do \_ sensor CIM**](cim-sensor.md), para 3 ("tensão").</span><span class="sxs-lookup"><span data-stu-id="3d24a-107">A voltage sensor can be defined by setting the **SensorType** property, inherited from [**CIM\_Sensor**](cim-sensor.md), to 3 ("Voltage").</span></span> <span data-ttu-id="3d24a-108">Outras propriedades dessa classe são embutidas em código para valores constantes que correspondem às definições na hierarquia do sensor.</span><span class="sxs-lookup"><span data-stu-id="3d24a-108">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d24a-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3d24a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d24a-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d24a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d24a-111">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3d24a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3d24a-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3d24a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d24a-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d24a-113">Syntax</span></span>

``` syntax
[UUID("{A998F9B4-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VoltageSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="3d24a-114">Membros</span><span class="sxs-lookup"><span data-stu-id="3d24a-114">Members</span></span>

<span data-ttu-id="3d24a-115">A classe **CIM \_ voltagem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3d24a-115">The **CIM\_VoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="3d24a-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="3d24a-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="3d24a-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3d24a-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3d24a-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="3d24a-118">Methods</span></span>

<span data-ttu-id="3d24a-119">A classe **CIM \_ voltagem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3d24a-119">The **CIM\_VoltageSensor** class has these methods.</span></span>



| <span data-ttu-id="3d24a-120">Método</span><span class="sxs-lookup"><span data-stu-id="3d24a-120">Method</span></span>                                                                   | <span data-ttu-id="3d24a-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d24a-121">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d24a-122">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="3d24a-122">**Reset**</span></span>](reset-method-in-class-cim-voltagesensor.md)                 | <span data-ttu-id="3d24a-123">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="3d24a-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3d24a-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="3d24a-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3d24a-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md) | <span data-ttu-id="3d24a-126">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="3d24a-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3d24a-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3d24a-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3d24a-128">Properties</span></span>

<span data-ttu-id="3d24a-129">A classe **CIM \_ voltagem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3d24a-129">The **CIM\_VoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d24a-130">**Correta**</span><span class="sxs-lookup"><span data-stu-id="3d24a-130">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-133">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("exatidão"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,19 ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-134">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-134">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="3d24a-135">Seu valor é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="3d24a-135">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="3d24a-136">Essa propriedade e as propriedades de **resolução** e **tolerância** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-136">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="3d24a-137">A precisão pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-137">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="3d24a-138">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-138">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-139">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="3d24a-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d24a-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-142">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-143">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-143">Availability and status of the device.</span></span>

<span data-ttu-id="3d24a-144">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d24a-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3d24a-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d24a-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3d24a-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3d24a-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="3d24a-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-148">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="3d24a-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3d24a-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="3d24a-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3d24a-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="3d24a-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3d24a-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="3d24a-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3d24a-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="3d24a-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3d24a-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="3d24a-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3d24a-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="3d24a-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3d24a-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="3d24a-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3d24a-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="3d24a-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3d24a-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="3d24a-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3d24a-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="3d24a-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-159">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3d24a-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3d24a-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="3d24a-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-161">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3d24a-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="3d24a-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-163">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3d24a-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="3d24a-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3d24a-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="3d24a-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-166">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="3d24a-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3d24a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="3d24a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-168">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="3d24a-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3d24a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="3d24a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-170">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="3d24a-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3d24a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="3d24a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-172">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3d24a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="3d24a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-174">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="3d24a-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d24a-175">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3d24a-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-178">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3d24a-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-179">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3d24a-179">Short textual description of the object.</span></span>

<span data-ttu-id="3d24a-180">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3d24a-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-184">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3d24a-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-185">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3d24a-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="3d24a-186">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3d24a-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3d24a-188"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="3d24a-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-189">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3d24a-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3d24a-191">(1)</span><span class="sxs-lookup"><span data-stu-id="3d24a-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-192">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3d24a-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3d24a-194">(2)</span><span class="sxs-lookup"><span data-stu-id="3d24a-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3d24a-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3d24a-196">(3)</span><span class="sxs-lookup"><span data-stu-id="3d24a-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-197">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="3d24a-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3d24a-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3d24a-199">(4)</span><span class="sxs-lookup"><span data-stu-id="3d24a-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-200">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-200">Device is not working properly.</span></span> <span data-ttu-id="3d24a-201">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3d24a-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3d24a-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3d24a-203">(5)</span><span class="sxs-lookup"><span data-stu-id="3d24a-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-204">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="3d24a-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3d24a-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3d24a-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="3d24a-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-207">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3d24a-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3d24a-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3d24a-209">(7)</span><span class="sxs-lookup"><span data-stu-id="3d24a-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3d24a-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3d24a-211">(8)</span><span class="sxs-lookup"><span data-stu-id="3d24a-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-212">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3d24a-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3d24a-214">(9)</span><span class="sxs-lookup"><span data-stu-id="3d24a-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-215">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-215">Device is not working properly.</span></span> <span data-ttu-id="3d24a-216">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3d24a-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3d24a-218">(10)</span><span class="sxs-lookup"><span data-stu-id="3d24a-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-219">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3d24a-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3d24a-221">(11)</span><span class="sxs-lookup"><span data-stu-id="3d24a-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-222">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3d24a-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3d24a-224">12</span><span class="sxs-lookup"><span data-stu-id="3d24a-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-225">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="3d24a-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3d24a-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3d24a-227">(13)</span><span class="sxs-lookup"><span data-stu-id="3d24a-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-228">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3d24a-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3d24a-230">(14)</span><span class="sxs-lookup"><span data-stu-id="3d24a-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-231">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3d24a-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3d24a-233">(15)</span><span class="sxs-lookup"><span data-stu-id="3d24a-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-234">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="3d24a-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3d24a-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3d24a-236">(16)</span><span class="sxs-lookup"><span data-stu-id="3d24a-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-237">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="3d24a-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3d24a-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3d24a-239">(17)</span><span class="sxs-lookup"><span data-stu-id="3d24a-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-240">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3d24a-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3d24a-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3d24a-242">(18)</span><span class="sxs-lookup"><span data-stu-id="3d24a-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-243">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="3d24a-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3d24a-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3d24a-245">(19)</span><span class="sxs-lookup"><span data-stu-id="3d24a-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3d24a-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3d24a-247">(20)</span><span class="sxs-lookup"><span data-stu-id="3d24a-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-248">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3d24a-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3d24a-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3d24a-250">(21)</span><span class="sxs-lookup"><span data-stu-id="3d24a-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-251">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="3d24a-251">System failure.</span></span> <span data-ttu-id="3d24a-252">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="3d24a-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3d24a-253">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3d24a-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3d24a-255">(22)</span><span class="sxs-lookup"><span data-stu-id="3d24a-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-256">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3d24a-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3d24a-258">(23)</span><span class="sxs-lookup"><span data-stu-id="3d24a-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-259">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="3d24a-259">System failure.</span></span> <span data-ttu-id="3d24a-260">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="3d24a-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3d24a-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3d24a-262">(24)</span><span class="sxs-lookup"><span data-stu-id="3d24a-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-263">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="3d24a-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3d24a-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3d24a-265">(25)</span><span class="sxs-lookup"><span data-stu-id="3d24a-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-266">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3d24a-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3d24a-268">(26)</span><span class="sxs-lookup"><span data-stu-id="3d24a-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-269">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3d24a-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3d24a-271">(27)</span><span class="sxs-lookup"><span data-stu-id="3d24a-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-272">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3d24a-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3d24a-274">(28)</span><span class="sxs-lookup"><span data-stu-id="3d24a-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-275">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="3d24a-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3d24a-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3d24a-277">(29)</span><span class="sxs-lookup"><span data-stu-id="3d24a-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-278">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-278">Device is disabled.</span></span> <span data-ttu-id="3d24a-279">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="3d24a-279">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3d24a-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3d24a-281">(30)</span><span class="sxs-lookup"><span data-stu-id="3d24a-281">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-282">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="3d24a-282">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3d24a-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3d24a-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3d24a-284">(31)</span><span class="sxs-lookup"><span data-stu-id="3d24a-284">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-285">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-285">Device is not working properly.</span></span> <span data-ttu-id="3d24a-286">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="3d24a-286">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d24a-287">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="3d24a-287">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-288">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3d24a-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-290">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3d24a-290">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-291">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3d24a-291">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3d24a-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-293">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3d24a-293">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-296">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d24a-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-297">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="3d24a-297">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3d24a-298">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="3d24a-298">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3d24a-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-300">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="3d24a-300">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-301">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-301">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-303">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-303">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-304">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="3d24a-304">Current value indicated by the sensor.</span></span>

<span data-ttu-id="3d24a-305">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-306">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3d24a-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-307">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-309">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="3d24a-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-310">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3d24a-310">Textual description of the object.</span></span>

<span data-ttu-id="3d24a-311">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3d24a-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-315">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d24a-315">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-316">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-316">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="3d24a-317">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3d24a-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-319">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3d24a-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-321">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="3d24a-321">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="3d24a-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3d24a-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-326">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="3d24a-326">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="3d24a-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3d24a-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-329">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3d24a-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-331">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-332">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-332">Date and time the object was installed.</span></span> <span data-ttu-id="3d24a-333">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3d24a-334">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-335">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="3d24a-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-336">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3d24a-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-338">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="3d24a-339">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3d24a-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-341">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-343">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3d24a-344">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="3d24a-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-346">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-348">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-348">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-349">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="3d24a-349">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="3d24a-350">Se a propriedade **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-350">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="3d24a-351">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="3d24a-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-353">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-355">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-355">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-356">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="3d24a-356">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="3d24a-357">Se a propriedade **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="3d24a-357">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="3d24a-358">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="3d24a-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-360">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-362">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-362">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-363">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="3d24a-363">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="3d24a-364">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="3d24a-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="3d24a-365">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-365">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="3d24a-366">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="3d24a-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-368">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-370">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-371">Maior valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="3d24a-372">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="3d24a-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-374">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-376">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-376">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-377">Menor valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="3d24a-378">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-379">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3d24a-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-380">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-382">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3d24a-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-383">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="3d24a-383">Label by which the object is known.</span></span> <span data-ttu-id="3d24a-384">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="3d24a-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3d24a-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="3d24a-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-387">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-389">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-390">Valor esperado ou normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-390">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="3d24a-391">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="3d24a-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-393">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-395">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-395">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-396">Intervalo máximo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-396">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="3d24a-397">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="3d24a-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-399">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-401">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-401">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-402">Intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-402">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="3d24a-403">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3d24a-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-405">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-407">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3d24a-407">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-408">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-408">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="3d24a-409">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3d24a-410">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3d24a-410">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3d24a-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-412">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d24a-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-414">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3d24a-415">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="3d24a-415">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d24a-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3d24a-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3d24a-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3d24a-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3d24a-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3d24a-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3d24a-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3d24a-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-420">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3d24a-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3d24a-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="3d24a-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-422">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="3d24a-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3d24a-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="3d24a-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-424">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="3d24a-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3d24a-425">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="3d24a-426">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="3d24a-426">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3d24a-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="3d24a-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-428">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="3d24a-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3d24a-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="3d24a-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3d24a-430">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="3d24a-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3d24a-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3d24a-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-432">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3d24a-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-433">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-434">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="3d24a-434">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="3d24a-435">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="3d24a-435">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="3d24a-436">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="3d24a-436">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="3d24a-437">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="3d24a-437">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="3d24a-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-439">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="3d24a-439">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-440">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-440">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-442">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimos de milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-443">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-443">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="3d24a-444">Essa propriedade e as propriedades de **precisão** e **tolerância** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-444">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="3d24a-445">Esse valor pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-445">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="3d24a-446">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-446">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-447">**Status**</span><span class="sxs-lookup"><span data-stu-id="3d24a-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-450">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3d24a-450">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-451">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3d24a-451">Current status of the object.</span></span>

<span data-ttu-id="3d24a-452">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3d24a-453">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3d24a-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3d24a-454">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3d24a-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3d24a-455">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="3d24a-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3d24a-456">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3d24a-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d24a-457">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3d24a-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3d24a-458">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3d24a-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3d24a-459">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="3d24a-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3d24a-460">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="3d24a-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3d24a-461">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="3d24a-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3d24a-462">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="3d24a-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3d24a-463">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3d24a-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3d24a-464">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="3d24a-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3d24a-465">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="3d24a-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d24a-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3d24a-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-467">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d24a-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-469">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-470">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-470">State of the logical device.</span></span> <span data-ttu-id="3d24a-471">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="3d24a-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3d24a-472">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3d24a-473">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3d24a-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3d24a-474">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3d24a-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3d24a-475">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3d24a-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3d24a-476">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="3d24a-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3d24a-477">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="3d24a-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d24a-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3d24a-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-479">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-481">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d24a-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-482">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-482">Scoping system's creation class name.</span></span>

<span data-ttu-id="3d24a-483">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3d24a-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-485">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3d24a-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-487">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d24a-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-488">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="3d24a-488">Scoping system's name.</span></span>

<span data-ttu-id="3d24a-489">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-490">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="3d24a-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-491">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-493">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("tolerância"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-494">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="3d24a-495">Essa propriedade e as propriedades de **resolução** e **precisão** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="3d24a-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="3d24a-496">A tolerância pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="3d24a-497">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-497">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-498">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="3d24a-498">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-499">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-499">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-501">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-501">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-502">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="3d24a-502">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="3d24a-503">Se a propriedade **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-503">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="3d24a-504">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-504">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-505">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="3d24a-505">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-506">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-506">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-508">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-508">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-509">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="3d24a-509">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="3d24a-510">Se a propriedade **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="3d24a-510">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="3d24a-511">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-511">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d24a-512">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="3d24a-512">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d24a-513">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3d24a-513">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d24a-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d24a-515">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de tensão DMTF \| 1,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="3d24a-515">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3d24a-516">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="3d24a-516">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="3d24a-517">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="3d24a-517">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="3d24a-518">Se a propriedade **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="3d24a-518">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="3d24a-519">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-519">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d24a-520">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d24a-520">Remarks</span></span>

<span data-ttu-id="3d24a-521">A classe **CIM \_ voltagem** é derivada do [**\_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-521">The **CIM\_VoltageSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="3d24a-522">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3d24a-522">WMI does not implement this class.</span></span> <span data-ttu-id="3d24a-523">Para classes WMI derivadas do **CIM \_ voltagem**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3d24a-523">For WMI classes derived from **CIM\_VoltageSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3d24a-524">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3d24a-524">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d24a-525">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3d24a-525">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d24a-526">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d24a-526">Requirements</span></span>



| <span data-ttu-id="3d24a-527">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d24a-527">Requirement</span></span> | <span data-ttu-id="3d24a-528">Valor</span><span class="sxs-lookup"><span data-stu-id="3d24a-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d24a-529">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d24a-529">Minimum supported client</span></span><br/> | <span data-ttu-id="3d24a-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d24a-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d24a-531">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d24a-531">Minimum supported server</span></span><br/> | <span data-ttu-id="3d24a-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d24a-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d24a-533">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d24a-533">Namespace</span></span><br/>                | <span data-ttu-id="3d24a-534">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d24a-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d24a-535">MOF</span><span class="sxs-lookup"><span data-stu-id="3d24a-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d24a-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d24a-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d24a-537">DLL</span><span class="sxs-lookup"><span data-stu-id="3d24a-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d24a-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d24a-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d24a-539">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d24a-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d24a-540">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3d24a-540">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

