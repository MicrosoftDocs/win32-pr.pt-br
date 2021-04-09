---
description: A \_ classe CIM CurrentSensor existe para compatibilidade com versões anteriores de definições de esquema CIM.
ms.assetid: d1835b09-4286-4586-92ec-f5f77791aea6
ms.tgt_platform: multiple
title: Classe CIM_CurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor
- CIM_CurrentSensor.Accuracy
- CIM_CurrentSensor.Availability
- CIM_CurrentSensor.Caption
- CIM_CurrentSensor.ConfigManagerErrorCode
- CIM_CurrentSensor.ConfigManagerUserConfig
- CIM_CurrentSensor.CreationClassName
- CIM_CurrentSensor.CurrentReading
- CIM_CurrentSensor.Description
- CIM_CurrentSensor.DeviceID
- CIM_CurrentSensor.ErrorCleared
- CIM_CurrentSensor.ErrorDescription
- CIM_CurrentSensor.InstallDate
- CIM_CurrentSensor.IsLinear
- CIM_CurrentSensor.LastErrorCode
- CIM_CurrentSensor.LowerThresholdCritical
- CIM_CurrentSensor.LowerThresholdFatal
- CIM_CurrentSensor.LowerThresholdNonCritical
- CIM_CurrentSensor.MaxReadable
- CIM_CurrentSensor.MinReadable
- CIM_CurrentSensor.Name
- CIM_CurrentSensor.NominalReading
- CIM_CurrentSensor.NormalMax
- CIM_CurrentSensor.NormalMin
- CIM_CurrentSensor.PNPDeviceID
- CIM_CurrentSensor.PowerManagementCapabilities
- CIM_CurrentSensor.PowerManagementSupported
- CIM_CurrentSensor.Resolution
- CIM_CurrentSensor.Status
- CIM_CurrentSensor.StatusInfo
- CIM_CurrentSensor.SystemCreationClassName
- CIM_CurrentSensor.SystemName
- CIM_CurrentSensor.Tolerance
- CIM_CurrentSensor.UpperThresholdCritical
- CIM_CurrentSensor.UpperThresholdFatal
- CIM_CurrentSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1fe2a34e2e598d5c9655abbf84324dbf9982e416
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089295"
---
# <a name="cim_currentsensor-class"></a><span data-ttu-id="0547f-103">\_Classe CIM CurrentSensor</span><span class="sxs-lookup"><span data-stu-id="0547f-103">CIM\_CurrentSensor class</span></span>

<span data-ttu-id="0547f-104">A classe **CIM \_ CurrentSensor** existe para compatibilidade com versões anteriores de definições de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="0547f-104">The **CIM\_CurrentSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span>

<span data-ttu-id="0547f-105">As adições [**ao \_ sensor CIM**](cim-sensor.md) e o [**\_ NumericSensor do CIM**](cim-numericsensor.md) na versão 2,2 o tornam não mais necessário.</span><span class="sxs-lookup"><span data-stu-id="0547f-105">Additions to [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) in version 2.2 make it no longer necessary.</span></span> <span data-ttu-id="0547f-106">Uma classe **CIM \_ CurrentSensor** pode ser definida definindo a propriedade **SensorType** , herdada do **\_ sensor CIM**, para 4 ("atual").</span><span class="sxs-lookup"><span data-stu-id="0547f-106">A **CIM\_CurrentSensor** class can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 4 ("Current").</span></span> <span data-ttu-id="0547f-107">Outras propriedades dessa classe são embutidas em código para valores constantes, que correspondem às definições na hierarquia do sensor.</span><span class="sxs-lookup"><span data-stu-id="0547f-107">Other properties of this class are hard-coded to constant values, which correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0547f-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0547f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0547f-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0547f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0547f-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0547f-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0547f-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0547f-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0547f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0547f-112">Syntax</span></span>

``` syntax
[UUID("{DCA1D084-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_CurrentSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="0547f-113">Membros</span><span class="sxs-lookup"><span data-stu-id="0547f-113">Members</span></span>

<span data-ttu-id="0547f-114">A classe **CIM \_ CurrentSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0547f-114">The **CIM\_CurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="0547f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="0547f-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="0547f-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0547f-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0547f-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="0547f-117">Methods</span></span>

<span data-ttu-id="0547f-118">A classe **CIM \_ CurrentSensor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0547f-118">The **CIM\_CurrentSensor** class has these methods.</span></span>



| <span data-ttu-id="0547f-119">Método</span><span class="sxs-lookup"><span data-stu-id="0547f-119">Method</span></span>                                                                   | <span data-ttu-id="0547f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="0547f-120">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0547f-121">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0547f-121">**Reset**</span></span>](reset-method-in-class-cim-currentsensor.md)                 | <span data-ttu-id="0547f-122">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0547f-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="0547f-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0547f-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0547f-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0547f-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-currentsensor.md) | <span data-ttu-id="0547f-125">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="0547f-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0547f-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0547f-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0547f-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0547f-127">Properties</span></span>

<span data-ttu-id="0547f-128">A classe **CIM \_ CurrentSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0547f-128">The **CIM\_CurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0547f-129">**Correta**</span><span class="sxs-lookup"><span data-stu-id="0547f-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-130">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("exatidão"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,19 ")</span><span class="sxs-lookup"><span data-stu-id="0547f-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-133">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="0547f-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="0547f-134">Seu valor é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="0547f-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="0547f-135">Essa propriedade e as propriedades de **resolução** e **tolerância** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="0547f-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="0547f-136">A precisão pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0547f-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="0547f-137">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="0547f-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0547f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-141">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0547f-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-142">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-142">Availability and status of the device.</span></span>

<span data-ttu-id="0547f-143">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0547f-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0547f-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0547f-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0547f-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0547f-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0547f-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0547f-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0547f-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0547f-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="0547f-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0547f-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="0547f-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0547f-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="0547f-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0547f-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="0547f-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0547f-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="0547f-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0547f-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="0547f-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0547f-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="0547f-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0547f-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="0547f-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0547f-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="0547f-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-157">Economia de energia desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0547f-157">Power save   unknown.</span></span>

<span data-ttu-id="0547f-158">O dispositivo está em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0547f-158">Device is in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0547f-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="0547f-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-160">Economia de energia no modo de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="0547f-160">Power save   low-power mode.</span></span>

<span data-ttu-id="0547f-161">O dispositivo está em um modo de economia de energia e ainda está funcionando, mas pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="0547f-161">Device is in a power-save mode and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0547f-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="0547f-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-163">Power Save em espera.</span><span class="sxs-lookup"><span data-stu-id="0547f-163">Power save   standby.</span></span>

<span data-ttu-id="0547f-164">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0547f-164">Device is not functioning, but it could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0547f-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="0547f-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0547f-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0547f-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-167">Aviso de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0547f-167">Power save   warning.</span></span>

<span data-ttu-id="0547f-168">O dispositivo está em um estado de aviso e em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0547f-168">Device is in a warning state and a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0547f-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0547f-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0547f-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0547f-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0547f-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="0547f-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0547f-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="0547f-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-173">O sensor atual não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0547f-173">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0547f-174">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0547f-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-177">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0547f-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-178">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0547f-178">Short textual description of the object.</span></span>

<span data-ttu-id="0547f-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0547f-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-181">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0547f-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-183">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0547f-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-184">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0547f-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0547f-185">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0547f-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0547f-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0547f-187"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="0547f-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-188">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0547f-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0547f-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0547f-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0547f-190">(1)</span><span class="sxs-lookup"><span data-stu-id="0547f-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-191">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="0547f-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0547f-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0547f-193">(2)</span><span class="sxs-lookup"><span data-stu-id="0547f-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0547f-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="0547f-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0547f-195">(3)</span><span class="sxs-lookup"><span data-stu-id="0547f-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-196">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="0547f-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0547f-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0547f-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0547f-198">(4)</span><span class="sxs-lookup"><span data-stu-id="0547f-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-199">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0547f-199">Device is not working properly.</span></span> <span data-ttu-id="0547f-200">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0547f-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0547f-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="0547f-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0547f-202">(5)</span><span class="sxs-lookup"><span data-stu-id="0547f-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-203">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="0547f-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0547f-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="0547f-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0547f-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="0547f-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-206">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0547f-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0547f-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="0547f-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0547f-208">(7)</span><span class="sxs-lookup"><span data-stu-id="0547f-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0547f-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="0547f-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0547f-210">(8)</span><span class="sxs-lookup"><span data-stu-id="0547f-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-211">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="0547f-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0547f-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="0547f-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0547f-213">(9)</span><span class="sxs-lookup"><span data-stu-id="0547f-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-214">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-214">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0547f-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="0547f-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0547f-216">(10)</span><span class="sxs-lookup"><span data-stu-id="0547f-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-217">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0547f-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="0547f-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0547f-219">(11)</span><span class="sxs-lookup"><span data-stu-id="0547f-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-220">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0547f-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="0547f-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0547f-222">12</span><span class="sxs-lookup"><span data-stu-id="0547f-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-223">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="0547f-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0547f-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0547f-225">(13)</span><span class="sxs-lookup"><span data-stu-id="0547f-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-226">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0547f-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="0547f-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0547f-228">(14)</span><span class="sxs-lookup"><span data-stu-id="0547f-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-229">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="0547f-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0547f-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="0547f-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0547f-231">(15)</span><span class="sxs-lookup"><span data-stu-id="0547f-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-232">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="0547f-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0547f-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="0547f-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0547f-234">(16)</span><span class="sxs-lookup"><span data-stu-id="0547f-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-235">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="0547f-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0547f-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="0547f-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0547f-237">(17)</span><span class="sxs-lookup"><span data-stu-id="0547f-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-238">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0547f-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0547f-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0547f-240">(18)</span><span class="sxs-lookup"><span data-stu-id="0547f-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-241">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="0547f-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0547f-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="0547f-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0547f-243">(19)</span><span class="sxs-lookup"><span data-stu-id="0547f-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0547f-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0547f-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0547f-245">(20)</span><span class="sxs-lookup"><span data-stu-id="0547f-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-246">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0547f-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0547f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0547f-248">(21)</span><span class="sxs-lookup"><span data-stu-id="0547f-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-249">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0547f-249">System failure.</span></span> <span data-ttu-id="0547f-250">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0547f-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0547f-251">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0547f-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="0547f-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0547f-253">(22)</span><span class="sxs-lookup"><span data-stu-id="0547f-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-254">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0547f-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0547f-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="0547f-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0547f-256">(23)</span><span class="sxs-lookup"><span data-stu-id="0547f-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-257">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0547f-257">System failure.</span></span> <span data-ttu-id="0547f-258">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0547f-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0547f-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="0547f-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0547f-260">(24)</span><span class="sxs-lookup"><span data-stu-id="0547f-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-261">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="0547f-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0547f-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0547f-263">(25)</span><span class="sxs-lookup"><span data-stu-id="0547f-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-264">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0547f-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0547f-266">(26)</span><span class="sxs-lookup"><span data-stu-id="0547f-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-267">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0547f-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0547f-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="0547f-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0547f-269">(27)</span><span class="sxs-lookup"><span data-stu-id="0547f-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-270">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="0547f-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0547f-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="0547f-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0547f-272">(28)</span><span class="sxs-lookup"><span data-stu-id="0547f-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-273">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="0547f-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0547f-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="0547f-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0547f-275">(29)</span><span class="sxs-lookup"><span data-stu-id="0547f-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-276">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="0547f-276">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0547f-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="0547f-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0547f-278">(30)</span><span class="sxs-lookup"><span data-stu-id="0547f-278">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-279">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="0547f-279">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0547f-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0547f-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0547f-281">(31)</span><span class="sxs-lookup"><span data-stu-id="0547f-281">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-282">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="0547f-282">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0547f-283">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0547f-283">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-284">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0547f-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-286">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0547f-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-287">Indica se o dispositivo está usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0547f-287">Indicates whether the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0547f-288">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-289">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0547f-289">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-292">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0547f-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0547f-293">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0547f-293">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0547f-294">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0547f-294">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0547f-295">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-296">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="0547f-296">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-297">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-297">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-299">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-299">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-300">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="0547f-300">Current value indicated by the sensor.</span></span>

<span data-ttu-id="0547f-301">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-301">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-302">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0547f-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-305">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0547f-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-306">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0547f-306">Textual description of the object.</span></span>

<span data-ttu-id="0547f-307">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0547f-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-309">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-311">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0547f-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0547f-312">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0547f-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0547f-313">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0547f-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-315">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0547f-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0547f-317">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="0547f-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0547f-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0547f-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-320">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0547f-322">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="0547f-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0547f-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0547f-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-325">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0547f-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-327">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0547f-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-328">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="0547f-328">Date and time when the object was installed.</span></span> <span data-ttu-id="0547f-329">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0547f-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0547f-330">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-331">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="0547f-331">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-332">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0547f-332">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-333">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0547f-334">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0547f-334">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="0547f-335">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-335">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0547f-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-337">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0547f-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0547f-339">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0547f-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0547f-340">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-341">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="0547f-341">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-342">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-342">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-344">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-344">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-345">Valor de limite que especifica se o sensor está operando sob condições críticas.</span><span class="sxs-lookup"><span data-stu-id="0547f-345">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="0547f-346">Se a propriedade **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="0547f-346">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="0547f-347">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-347">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-348">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="0547f-348">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-349">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-349">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-351">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-351">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-352">Valor de limite que especifica se o sensor está operando sob condições fatais.</span><span class="sxs-lookup"><span data-stu-id="0547f-352">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="0547f-353">Se a propriedade **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="0547f-353">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="0547f-354">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-354">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-355">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="0547f-355">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-356">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-356">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-358">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-358">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-359">Valor de limite que especifica se o sensor está operando em condições normais ou não críticas.</span><span class="sxs-lookup"><span data-stu-id="0547f-359">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="0547f-360">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="0547f-360">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="0547f-361">No entanto, se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="0547f-361">If the **CurrentReading** property, however, is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="0547f-362">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-362">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-363">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="0547f-363">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-364">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-364">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-366">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-366">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-367">Maior valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="0547f-367">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="0547f-368">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-368">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-369">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="0547f-369">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-370">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-370">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-372">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-372">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-373">Menor valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="0547f-373">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="0547f-374">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-374">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-375">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0547f-375">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-378">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0547f-378">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-379">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0547f-379">Label by which the object is known.</span></span> <span data-ttu-id="0547f-380">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="0547f-380">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0547f-381">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-381">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-382">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="0547f-382">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-383">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-383">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-384">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-385">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-385">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-386">Valor esperado para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="0547f-386">Expected value for the numeric sensor.</span></span>

<span data-ttu-id="0547f-387">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-387">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-388">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="0547f-388">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-389">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-389">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-391">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-391">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-392">Intervalo máximo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="0547f-392">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="0547f-393">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-393">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-394">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="0547f-394">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-395">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-395">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-397">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-397">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-398">Intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="0547f-398">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="0547f-399">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-399">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-400">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0547f-400">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-401">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-403">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0547f-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-404">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0547f-404">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0547f-405">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0547f-405">Example: "\*PNP030b"</span></span>

<span data-ttu-id="0547f-406">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0547f-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-408">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0547f-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0547f-409">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0547f-410">Recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0547f-410">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="0547f-411">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0547f-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0547f-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0547f-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0547f-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0547f-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0547f-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0547f-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0547f-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-416">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0547f-416">Power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0547f-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0547f-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-418">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="0547f-418">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0547f-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="0547f-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-420">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="0547f-420">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0547f-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="0547f-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-422">O método [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="0547f-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0547f-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="0547f-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0547f-424">O método [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="0547f-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0547f-425">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0547f-425">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-426">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0547f-426">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-427">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0547f-428">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0547f-428">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0547f-429">Essa propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento ou, se habilitado, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0547f-429">This property does not indicate that power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0547f-430">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0547f-430">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0547f-431">Se **for false**, o valor inteiro 1, para a cadeia de caracteres "sem suporte", deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0547f-431">If **FALSE**, the integer value 1, for the string "Not Supported", should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0547f-432">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-433">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="0547f-433">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-434">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0547f-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-436">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimos de milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-436">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-437">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="0547f-437">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="0547f-438">Essa propriedade e as propriedades de **precisão** e **tolerância** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="0547f-438">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="0547f-439">Esse valor pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0547f-439">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="0547f-440">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-440">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-441">**Status**</span><span class="sxs-lookup"><span data-stu-id="0547f-441">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-442">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-443">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-444">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0547f-444">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-445">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0547f-445">String that indicates the current status of the object.</span></span> <span data-ttu-id="0547f-446">Pode ser definido um status operacional e não operacional.</span><span class="sxs-lookup"><span data-stu-id="0547f-446">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="0547f-447">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="0547f-447">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0547f-448">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="0547f-448">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0547f-449">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="0547f-449">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0547f-450">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="0547f-450">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0547f-451">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="0547f-451">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0547f-452">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0547f-453">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0547f-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0547f-454">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0547f-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0547f-455">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0547f-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0547f-456">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0547f-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0547f-457">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0547f-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0547f-458">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0547f-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0547f-459">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0547f-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0547f-460">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0547f-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0547f-461">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0547f-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0547f-462">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0547f-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0547f-463">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0547f-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0547f-464">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0547f-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0547f-465">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0547f-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0547f-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0547f-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-467">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0547f-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-469">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="0547f-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-470">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0547f-470">State of the logical device.</span></span> <span data-ttu-id="0547f-471">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="0547f-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0547f-472">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0547f-473">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0547f-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0547f-474">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0547f-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0547f-475">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0547f-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0547f-476">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="0547f-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0547f-477">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="0547f-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0547f-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0547f-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-479">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-481">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0547f-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0547f-482">Propriedade **CreationClassName** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0547f-482">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="0547f-483">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0547f-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-485">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0547f-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-486">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-487">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0547f-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0547f-488">Propriedade de **nome** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0547f-488">Scoping system's **Name** property.</span></span>

<span data-ttu-id="0547f-489">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-490">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="0547f-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-491">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-492">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-493">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("tolerância"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-494">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="0547f-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="0547f-495">Essa propriedade e as propriedades de **resolução** e **precisão** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="0547f-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="0547f-496">A tolerância pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0547f-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="0547f-497">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="0547f-497">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-498">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-498">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-500">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-500">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-501">Valor de limite que especifica se o sensor está operando sob condições críticas.</span><span class="sxs-lookup"><span data-stu-id="0547f-501">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="0547f-502">Se a propriedade **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="0547f-502">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="0547f-503">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-503">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-504">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="0547f-504">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-505">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-505">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-506">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-507">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-507">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-508">Valor de limite que especifica se o sensor está operando sob condições fatais.</span><span class="sxs-lookup"><span data-stu-id="0547f-508">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="0547f-509">Se a propriedade **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="0547f-509">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="0547f-510">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-510">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="0547f-511">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="0547f-511">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0547f-512">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0547f-512">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0547f-513">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0547f-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0547f-514">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Investigação de corrente elétrica de DMTF \| 1,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliamps ")</span><span class="sxs-lookup"><span data-stu-id="0547f-514">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="0547f-515">Valor de limite que especifica se o sensor está operando em condições normais ou não críticas.</span><span class="sxs-lookup"><span data-stu-id="0547f-515">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="0547f-516">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="0547f-516">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="0547f-517">No entanto, se a propriedade **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="0547f-517">If the **CurrentReading** property, however, is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="0547f-518">Essa propriedade é herdada [**de \_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-518">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0547f-519">Comentários</span><span class="sxs-lookup"><span data-stu-id="0547f-519">Remarks</span></span>

<span data-ttu-id="0547f-520">A classe **CIM \_ CurrentSensor** é derivada do [**\_ NumericSensor de CIM**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-520">The **CIM\_CurrentSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="0547f-521">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0547f-521">WMI does not implement this class.</span></span> <span data-ttu-id="0547f-522">Para obter mais informações sobre classes WMI derivadas do **CIM \_ CurrentSensor**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0547f-522">For more information about WMI classes derived from **CIM\_CurrentSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0547f-523">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0547f-523">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0547f-524">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0547f-524">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0547f-525">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0547f-525">Requirements</span></span>



| <span data-ttu-id="0547f-526">Requisito</span><span class="sxs-lookup"><span data-stu-id="0547f-526">Requirement</span></span> | <span data-ttu-id="0547f-527">Valor</span><span class="sxs-lookup"><span data-stu-id="0547f-527">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0547f-528">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0547f-528">Minimum supported client</span></span><br/> | <span data-ttu-id="0547f-529">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0547f-529">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0547f-530">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0547f-530">Minimum supported server</span></span><br/> | <span data-ttu-id="0547f-531">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0547f-531">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0547f-532">Namespace</span><span class="sxs-lookup"><span data-stu-id="0547f-532">Namespace</span></span><br/>                | <span data-ttu-id="0547f-533">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0547f-533">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0547f-534">MOF</span><span class="sxs-lookup"><span data-stu-id="0547f-534">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0547f-535"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0547f-535"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0547f-536">DLL</span><span class="sxs-lookup"><span data-stu-id="0547f-536">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0547f-537"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0547f-537"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0547f-538">Confira também</span><span class="sxs-lookup"><span data-stu-id="0547f-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0547f-539">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="0547f-539">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

