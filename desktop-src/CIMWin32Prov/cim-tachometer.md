---
description: A \_ classe do tacômetro CIM existe para compatibilidade com versões anteriores de definições de esquema CIM.
ms.assetid: 30b7c23e-05c6-4fd6-80bc-3f729855ab45
ms.tgt_platform: multiple
title: Classe CIM_Tachometer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Tachometer
- CIM_Tachometer.Accuracy
- CIM_Tachometer.Availability
- CIM_Tachometer.Caption
- CIM_Tachometer.ConfigManagerErrorCode
- CIM_Tachometer.ConfigManagerUserConfig
- CIM_Tachometer.CreationClassName
- CIM_Tachometer.CurrentReading
- CIM_Tachometer.Description
- CIM_Tachometer.DeviceID
- CIM_Tachometer.ErrorCleared
- CIM_Tachometer.ErrorDescription
- CIM_Tachometer.InstallDate
- CIM_Tachometer.IsLinear
- CIM_Tachometer.LastErrorCode
- CIM_Tachometer.LowerThresholdCritical
- CIM_Tachometer.LowerThresholdFatal
- CIM_Tachometer.LowerThresholdNonCritical
- CIM_Tachometer.MaxReadable
- CIM_Tachometer.MinReadable
- CIM_Tachometer.Name
- CIM_Tachometer.NominalReading
- CIM_Tachometer.NormalMax
- CIM_Tachometer.NormalMin
- CIM_Tachometer.PNPDeviceID
- CIM_Tachometer.PowerManagementCapabilities
- CIM_Tachometer.PowerManagementSupported
- CIM_Tachometer.Resolution
- CIM_Tachometer.Status
- CIM_Tachometer.StatusInfo
- CIM_Tachometer.SystemCreationClassName
- CIM_Tachometer.SystemName
- CIM_Tachometer.Tolerance
- CIM_Tachometer.UpperThresholdCritical
- CIM_Tachometer.UpperThresholdFatal
- CIM_Tachometer.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f761d7ef18ef7e27a46d6b5e8a5a00442752561
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755668"
---
# <a name="cim_tachometer-class"></a><span data-ttu-id="fa6d6-103">\_Classe de tacômetro CIM</span><span class="sxs-lookup"><span data-stu-id="fa6d6-103">CIM\_Tachometer class</span></span>

<span data-ttu-id="fa6d6-104">A classe do **\_ tacômetro CIM** existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-104">The **CIM\_Tachometer** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="fa6d6-105">Com adições às classes [**do \_ sensor CIM**](cim-sensor.md) e do [**cim \_ NumericSensor**](cim-numericsensor.md) na versão 2,2, ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="fa6d6-106">Um tacômetro pode ser definido definindo a propriedade **SensorType** , herdada do **\_ sensor CIM**, para 5 ("tacômetro").</span><span class="sxs-lookup"><span data-stu-id="fa6d6-106">A tachometer can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 5 ("Tachometer").</span></span> <span data-ttu-id="fa6d6-107">Outras propriedades dessa classe são embutidas em código para valores constantes que correspondem às definições na hierarquia do sensor.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-107">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa6d6-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa6d6-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa6d6-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fa6d6-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6d6-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa6d6-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{237D964F-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_Tachometer : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="fa6d6-113">Membros</span><span class="sxs-lookup"><span data-stu-id="fa6d6-113">Members</span></span>

<span data-ttu-id="fa6d6-114">A classe do **\_ tacômetro CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fa6d6-114">The **CIM\_Tachometer** class has these types of members:</span></span>

-   [<span data-ttu-id="fa6d6-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa6d6-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="fa6d6-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa6d6-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fa6d6-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="fa6d6-117">Methods</span></span>

<span data-ttu-id="fa6d6-118">A classe do **\_ tacômetro CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-118">The **CIM\_Tachometer** class has these methods.</span></span>



| <span data-ttu-id="fa6d6-119">Método</span><span class="sxs-lookup"><span data-stu-id="fa6d6-119">Method</span></span>                                                                | <span data-ttu-id="fa6d6-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa6d6-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa6d6-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-121">**Reset**</span></span>](reset-method-in-class-cim-tachometer.md)                 | <span data-ttu-id="fa6d6-122">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="fa6d6-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="fa6d6-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tachometer.md) | <span data-ttu-id="fa6d6-125">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="fa6d6-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fa6d6-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa6d6-127">Properties</span></span>

<span data-ttu-id="fa6d6-128">A classe do **\_ tacômetro CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-128">The **CIM\_Tachometer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa6d6-129">**Correta**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-130">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-132">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("centésimos de porcentagem")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-132">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-133">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="fa6d6-134">Seu valor é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="fa6d6-135">Essa propriedade e as propriedades de **resolução** e **tolerância** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="fa6d6-136">A precisão pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="fa6d6-137">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-141">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-142">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-142">Availability and status of the device.</span></span>

<span data-ttu-id="fa6d6-143">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa6d6-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa6d6-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="fa6d6-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-147">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="fa6d6-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="fa6d6-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="fa6d6-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fa6d6-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="fa6d6-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="fa6d6-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="fa6d6-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="fa6d6-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fa6d6-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="fa6d6-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="fa6d6-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="fa6d6-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-158">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="fa6d6-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-160">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="fa6d6-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-162">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-162">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="fa6d6-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="fa6d6-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-165">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="fa6d6-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-167">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="fa6d6-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-169">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="fa6d6-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-171">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="fa6d6-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-173">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa6d6-174">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-177">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-178">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-178">Short textual description of the object.</span></span>

<span data-ttu-id="fa6d6-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-183">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-184">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="fa6d6-185">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="fa6d6-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="fa6d6-187"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-188">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="fa6d6-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="fa6d6-190">(1)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-191">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fa6d6-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="fa6d6-193">(2)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="fa6d6-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="fa6d6-195">(3)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-196">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fa6d6-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="fa6d6-198">(4)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-199">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-199">Device is not working properly.</span></span> <span data-ttu-id="fa6d6-200">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="fa6d6-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="fa6d6-202">(5)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-203">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="fa6d6-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="fa6d6-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-206">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="fa6d6-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="fa6d6-208">(7)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="fa6d6-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="fa6d6-210">(8)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-211">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="fa6d6-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="fa6d6-213">(9)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-214">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-214">Device is not working properly.</span></span> <span data-ttu-id="fa6d6-215">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="fa6d6-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="fa6d6-217">(10)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-218">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="fa6d6-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="fa6d6-220">(11)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-221">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="fa6d6-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="fa6d6-223">12</span><span class="sxs-lookup"><span data-stu-id="fa6d6-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-224">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="fa6d6-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="fa6d6-226">(13)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-227">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="fa6d6-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="fa6d6-229">(14)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-230">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="fa6d6-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="fa6d6-232">(15)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-233">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="fa6d6-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="fa6d6-235">(16)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-236">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="fa6d6-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="fa6d6-238">(17)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-239">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fa6d6-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="fa6d6-241">(18)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-242">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="fa6d6-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="fa6d6-244">(19)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fa6d6-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="fa6d6-246">(20)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-247">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="fa6d6-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="fa6d6-249">(21)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-250">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-250">System failure.</span></span> <span data-ttu-id="fa6d6-251">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="fa6d6-252">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="fa6d6-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="fa6d6-254">(22)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-255">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="fa6d6-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="fa6d6-257">(23)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-258">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-258">System failure.</span></span> <span data-ttu-id="fa6d6-259">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="fa6d6-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="fa6d6-261">(24)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-262">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fa6d6-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="fa6d6-264">(25)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-265">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fa6d6-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="fa6d6-267">(26)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-268">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="fa6d6-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="fa6d6-270">(27)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-271">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="fa6d6-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="fa6d6-273">(28)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-274">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="fa6d6-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="fa6d6-276">(29)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-277">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-277">Device is disabled.</span></span> <span data-ttu-id="fa6d6-278">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="fa6d6-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="fa6d6-280">(30)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-281">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fa6d6-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="fa6d6-283">(31)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-284">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-284">Device is not working properly.</span></span> <span data-ttu-id="fa6d6-285">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa6d6-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-287">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-289">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-290">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="fa6d6-291">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-295">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-296">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fa6d6-297">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="fa6d6-298">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-299">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-300">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-302">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-303">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="fa6d6-304">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-305">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-308">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-309">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-309">Textual description of the object.</span></span>

<span data-ttu-id="fa6d6-310">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-311">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-314">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-315">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="fa6d6-316">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-317">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-318">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-320">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="fa6d6-321">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-325">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="fa6d6-326">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-328">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-330">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-331">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-331">Date and time the object was installed.</span></span> <span data-ttu-id="fa6d6-332">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="fa6d6-333">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-334">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-335">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-337">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="fa6d6-338">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-340">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-342">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="fa6d6-343">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-344">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-345">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-347">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-348">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="fa6d6-349">Se a propriedade **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="fa6d6-350">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-351">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-352">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-354">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-355">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="fa6d6-356">Se a propriedade **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="fa6d6-357">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-358">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-359">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-361">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-362">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="fa6d6-363">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="fa6d6-364">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="fa6d6-365">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-366">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-367">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-369">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-370">Maior valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="fa6d6-371">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-372">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-373">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-375">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-376">Menor valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="fa6d6-377">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-378">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-379">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-381">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-382">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-382">Label by which the object is known.</span></span> <span data-ttu-id="fa6d6-383">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fa6d6-384">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-385">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-386">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-388">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-389">Valor esperado ou normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="fa6d6-390">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-391">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-392">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-394">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-395">Intervalo máximo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="fa6d6-396">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-397">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-398">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-400">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-401">Intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="fa6d6-402">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-404">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-406">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-407">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="fa6d6-408">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="fa6d6-409">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="fa6d6-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-410">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-411">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-413">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="fa6d6-414">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa6d6-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fa6d6-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fa6d6-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fa6d6-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-419">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="fa6d6-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-421">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="fa6d6-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-423">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="fa6d6-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="fa6d6-424">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="fa6d6-425">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="fa6d6-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-427">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="fa6d6-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fa6d6-429">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa6d6-430">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-431">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-433">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="fa6d6-434">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fa6d6-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="fa6d6-435">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="fa6d6-436">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fa6d6-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="fa6d6-437">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-438">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-439">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-441">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("resolução"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("décimos de revoluçãos por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-442">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="fa6d6-443">Esse valor pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="fa6d6-444">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-445">**Status**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-446">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-448">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-449">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-449">Current status of the object.</span></span> <span data-ttu-id="fa6d6-450">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fa6d6-451">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fa6d6-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fa6d6-452">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fa6d6-453">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fa6d6-454">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa6d6-455">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fa6d6-456">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fa6d6-457">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fa6d6-458">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fa6d6-459">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fa6d6-460">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fa6d6-461">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fa6d6-462">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fa6d6-463">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa6d6-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-465">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-467">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-468">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-468">State of the logical device.</span></span> <span data-ttu-id="fa6d6-469">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="fa6d6-470">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa6d6-471">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa6d6-472">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fa6d6-473">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fa6d6-474">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fa6d6-475">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa6d6-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-477">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-479">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-480">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="fa6d6-481">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-483">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-485">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa6d6-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-486">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-486">Scoping system's name.</span></span>

<span data-ttu-id="fa6d6-487">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-488">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-489">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-491">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("tolerância"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-492">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="fa6d6-493">Essa propriedade e as propriedades de **resolução** e **precisão** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="fa6d6-494">A tolerância pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="fa6d6-495">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-496">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-497">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-498">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-499">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-500">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="fa6d6-501">Se a propriedade **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="fa6d6-502">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-503">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-504">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-505">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-506">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-507">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="fa6d6-508">Se a propriedade **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="fa6d6-509">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa6d6-510">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa6d6-511">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-512">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa6d6-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa6d6-513">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="fa6d6-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="fa6d6-514">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="fa6d6-515">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="fa6d6-516">Se a propriedade **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="fa6d6-517">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa6d6-518">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa6d6-518">Remarks</span></span>

<span data-ttu-id="fa6d6-519">A classe do **\_ tacômetro CIM** é derivada do [**\_ NumericSensor do CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="fa6d6-519">The **CIM\_Tachometer** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="fa6d6-520">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-520">WMI does not implement this class.</span></span>

<span data-ttu-id="fa6d6-521">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa6d6-522">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="fa6d6-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6d6-523">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa6d6-523">Requirements</span></span>



| <span data-ttu-id="fa6d6-524">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa6d6-524">Requirement</span></span> | <span data-ttu-id="fa6d6-525">Valor</span><span class="sxs-lookup"><span data-stu-id="fa6d6-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa6d6-526">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa6d6-526">Minimum supported client</span></span><br/> | <span data-ttu-id="fa6d6-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa6d6-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa6d6-528">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa6d6-528">Minimum supported server</span></span><br/> | <span data-ttu-id="fa6d6-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa6d6-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa6d6-530">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa6d6-530">Namespace</span></span><br/>                | <span data-ttu-id="fa6d6-531">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fa6d6-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa6d6-532">MOF</span><span class="sxs-lookup"><span data-stu-id="fa6d6-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa6d6-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa6d6-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa6d6-534">DLL</span><span class="sxs-lookup"><span data-stu-id="fa6d6-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa6d6-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa6d6-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa6d6-536">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa6d6-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6d6-537">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="fa6d6-537">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

