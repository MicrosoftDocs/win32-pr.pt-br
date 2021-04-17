---
description: A \_ classe CIM UninterruptiblePowerSupply representa os recursos e o gerenciamento de uma fonte de energia ininterrupta (UPS).
ms.assetid: 27ddc955-906b-40b9-981b-96872356477c
ms.tgt_platform: multiple
title: Classe CIM_UninterruptiblePowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply
- CIM_UninterruptiblePowerSupply.ActiveInputVoltage
- CIM_UninterruptiblePowerSupply.Availability
- CIM_UninterruptiblePowerSupply.Caption
- CIM_UninterruptiblePowerSupply.ConfigManagerErrorCode
- CIM_UninterruptiblePowerSupply.ConfigManagerUserConfig
- CIM_UninterruptiblePowerSupply.CreationClassName
- CIM_UninterruptiblePowerSupply.Description
- CIM_UninterruptiblePowerSupply.DeviceID
- CIM_UninterruptiblePowerSupply.ErrorCleared
- CIM_UninterruptiblePowerSupply.ErrorDescription
- CIM_UninterruptiblePowerSupply.EstimatedChargeRemaining
- CIM_UninterruptiblePowerSupply.EstimatedRunTime
- CIM_UninterruptiblePowerSupply.InstallDate
- CIM_UninterruptiblePowerSupply.IsSwitchingSupply
- CIM_UninterruptiblePowerSupply.LastErrorCode
- CIM_UninterruptiblePowerSupply.Name
- CIM_UninterruptiblePowerSupply.PNPDeviceID
- CIM_UninterruptiblePowerSupply.PowerManagementCapabilities
- CIM_UninterruptiblePowerSupply.PowerManagementSupported
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range1InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range1InputVoltageLow
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range2InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range2InputVoltageLow
- CIM_UninterruptiblePowerSupply.RemainingCapacityStatus
- CIM_UninterruptiblePowerSupply.Status
- CIM_UninterruptiblePowerSupply.StatusInfo
- CIM_UninterruptiblePowerSupply.SystemCreationClassName
- CIM_UninterruptiblePowerSupply.SystemName
- CIM_UninterruptiblePowerSupply.TimeOnBackup
- CIM_UninterruptiblePowerSupply.TotalOutputPower
- CIM_UninterruptiblePowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 214517fd6518cf2ca406523c61f522ae9c1adc46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749097"
---
# <a name="cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="56f1d-103">\_Classe CIM UninterruptiblePowerSupply</span><span class="sxs-lookup"><span data-stu-id="56f1d-103">CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="56f1d-104">A classe **CIM \_ UninterruptiblePowerSupply** representa os recursos e o gerenciamento de uma fonte de energia ininterrupta (UPS).</span><span class="sxs-lookup"><span data-stu-id="56f1d-104">The **CIM\_UninterruptiblePowerSupply** class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="56f1d-105">As propriedades do dispositivo UPS indicam quando a energia de entrada é cortada ou aumentada e as informações agregadas das baterias, geradores e assim por diante, que compõem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-105">The properties of the UPS device indicate when incoming power is trimmed or boosted, and the aggregated information of the batteries, generators, and so on, that make up the device.</span></span> <span data-ttu-id="56f1d-106">Os componentes individuais (por exemplo, várias baterias) também podem ser modelados de forma independente e associados ao UPS.</span><span class="sxs-lookup"><span data-stu-id="56f1d-106">The individual components (for example, multiple batteries) can also be independently modeled and associated with the UPS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56f1d-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="56f1d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="56f1d-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="56f1d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="56f1d-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="56f1d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="56f1d-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="56f1d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f1d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56f1d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UninterruptiblePowerSupply : CIM_PowerSupply
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  uint16   RemainingCapacityStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBackup;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="56f1d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="56f1d-112">Members</span></span>

<span data-ttu-id="56f1d-113">A classe **CIM \_ UninterruptiblePowerSupply** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="56f1d-113">The **CIM\_UninterruptiblePowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="56f1d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="56f1d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="56f1d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="56f1d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56f1d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="56f1d-116">Methods</span></span>

<span data-ttu-id="56f1d-117">A classe **CIM \_ UninterruptiblePowerSupply** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="56f1d-117">The **CIM\_UninterruptiblePowerSupply** class has these methods.</span></span>



| <span data-ttu-id="56f1d-118">Método</span><span class="sxs-lookup"><span data-stu-id="56f1d-118">Method</span></span>                                                                                | <span data-ttu-id="56f1d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="56f1d-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56f1d-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="56f1d-120">**Reset**</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)                 | <span data-ttu-id="56f1d-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56f1d-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="56f1d-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="56f1d-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="56f1d-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="56f1d-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md) | <span data-ttu-id="56f1d-124">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="56f1d-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="56f1d-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="56f1d-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="56f1d-126">Properties</span></span>

<span data-ttu-id="56f1d-127">A classe **CIM \_ UninterruptiblePowerSupply** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="56f1d-127">The **CIM\_UninterruptiblePowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56f1d-128">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="56f1d-128">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,15 ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-132">O intervalo de tensão de entrada está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="56f1d-132">Input voltage range is currently in use.</span></span> <span data-ttu-id="56f1d-133">Se o fornecimento não estiver atualmente desenhando energia, o valor 6 ("nenhum") poderá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-133">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="56f1d-134">Essas informações são necessárias no caso de um UPS, uma subclasse de fonte de [**alimentação \_ CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-134">This information is necessary in the case of a UPS, a subclass of [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="56f1d-135">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-135">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="56f1d-136">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-137">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-137">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="56f1d-138">**Intervalo 1** (3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-138">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="56f1d-139">**Intervalo 2** (4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-139">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="56f1d-140">**Ambos** (5)</span><span class="sxs-lookup"><span data-stu-id="56f1d-140">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="56f1d-141">**Nenhum** (6)</span><span class="sxs-lookup"><span data-stu-id="56f1d-141">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-142">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="56f1d-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-143">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-145">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-146">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-146">Availability and status of the device.</span></span>

<span data-ttu-id="56f1d-147">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="56f1d-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="56f1d-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-151">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="56f1d-151">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="56f1d-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="56f1d-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="56f1d-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="56f1d-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="56f1d-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="56f1d-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="56f1d-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="56f1d-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="56f1d-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="56f1d-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="56f1d-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="56f1d-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="56f1d-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="56f1d-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="56f1d-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="56f1d-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="56f1d-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="56f1d-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="56f1d-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-162">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="56f1d-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="56f1d-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="56f1d-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-164">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-164">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="56f1d-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="56f1d-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-166">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="56f1d-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="56f1d-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="56f1d-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="56f1d-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-169">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="56f1d-169">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="56f1d-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="56f1d-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-171">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="56f1d-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="56f1d-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="56f1d-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-173">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="56f1d-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="56f1d-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="56f1d-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-175">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="56f1d-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="56f1d-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-177">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="56f1d-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-178">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="56f1d-178">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-181">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="56f1d-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-182">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="56f1d-182">Short textual description of the object.</span></span>

<span data-ttu-id="56f1d-183">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-184">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="56f1d-184">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-185">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-185">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-187">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="56f1d-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-188">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="56f1d-188">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="56f1d-189">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-189">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="56f1d-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="56f1d-191"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="56f1d-191">(0)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-192">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-192">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="56f1d-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="56f1d-194">(1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-194">(1)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-195">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-195">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="56f1d-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="56f1d-197">(2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-197">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="56f1d-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="56f1d-199">(3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-199">(3)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-200">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="56f1d-200">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="56f1d-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="56f1d-202">(4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-203">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-203">Device is not working properly.</span></span> <span data-ttu-id="56f1d-204">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="56f1d-204">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="56f1d-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="56f1d-206">(5)</span><span class="sxs-lookup"><span data-stu-id="56f1d-206">(5)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-207">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="56f1d-207">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="56f1d-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="56f1d-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="56f1d-209">(6)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-210">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="56f1d-210">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="56f1d-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="56f1d-212">(7)</span><span class="sxs-lookup"><span data-stu-id="56f1d-212">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="56f1d-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="56f1d-214">(8)</span><span class="sxs-lookup"><span data-stu-id="56f1d-214">(8)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-215">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-215">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="56f1d-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="56f1d-217">(9)</span><span class="sxs-lookup"><span data-stu-id="56f1d-217">(9)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-218">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-218">Device is not working properly.</span></span> <span data-ttu-id="56f1d-219">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-219">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="56f1d-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="56f1d-221">(10)</span><span class="sxs-lookup"><span data-stu-id="56f1d-221">(10)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-222">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-222">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="56f1d-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="56f1d-224">(11)</span><span class="sxs-lookup"><span data-stu-id="56f1d-224">(11)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-225">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-225">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="56f1d-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="56f1d-227">12</span><span class="sxs-lookup"><span data-stu-id="56f1d-227">(12)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-228">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="56f1d-228">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="56f1d-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="56f1d-230">(13)</span><span class="sxs-lookup"><span data-stu-id="56f1d-230">(13)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-231">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-231">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="56f1d-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="56f1d-233">(14)</span><span class="sxs-lookup"><span data-stu-id="56f1d-233">(14)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-234">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-234">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="56f1d-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="56f1d-236">(15)</span><span class="sxs-lookup"><span data-stu-id="56f1d-236">(15)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-237">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="56f1d-237">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="56f1d-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="56f1d-239">(16)</span><span class="sxs-lookup"><span data-stu-id="56f1d-239">(16)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-240">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="56f1d-240">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="56f1d-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="56f1d-242">(17)</span><span class="sxs-lookup"><span data-stu-id="56f1d-242">(17)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-243">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="56f1d-243">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="56f1d-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="56f1d-245">(18)</span><span class="sxs-lookup"><span data-stu-id="56f1d-245">(18)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-246">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="56f1d-246">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="56f1d-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="56f1d-248">(19)</span><span class="sxs-lookup"><span data-stu-id="56f1d-248">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="56f1d-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="56f1d-250">(20)</span><span class="sxs-lookup"><span data-stu-id="56f1d-250">(20)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-251">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="56f1d-251">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="56f1d-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="56f1d-253">(21)</span><span class="sxs-lookup"><span data-stu-id="56f1d-253">(21)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-254">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="56f1d-254">System failure.</span></span> <span data-ttu-id="56f1d-255">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="56f1d-255">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="56f1d-256">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-256">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="56f1d-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="56f1d-258">(22)</span><span class="sxs-lookup"><span data-stu-id="56f1d-258">(22)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-259">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-259">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="56f1d-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="56f1d-261">(23)</span><span class="sxs-lookup"><span data-stu-id="56f1d-261">(23)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-262">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="56f1d-262">System failure.</span></span> <span data-ttu-id="56f1d-263">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="56f1d-263">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="56f1d-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="56f1d-265">(24)</span><span class="sxs-lookup"><span data-stu-id="56f1d-265">(24)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-266">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="56f1d-266">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="56f1d-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="56f1d-268">(25)</span><span class="sxs-lookup"><span data-stu-id="56f1d-268">(25)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-269">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="56f1d-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="56f1d-271">(26)</span><span class="sxs-lookup"><span data-stu-id="56f1d-271">(26)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-272">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="56f1d-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="56f1d-274">(27)</span><span class="sxs-lookup"><span data-stu-id="56f1d-274">(27)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-275">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="56f1d-275">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="56f1d-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="56f1d-277">(28)</span><span class="sxs-lookup"><span data-stu-id="56f1d-277">(28)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-278">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="56f1d-278">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="56f1d-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="56f1d-280">(29)</span><span class="sxs-lookup"><span data-stu-id="56f1d-280">(29)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-281">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-281">Device is disabled.</span></span> <span data-ttu-id="56f1d-282">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="56f1d-282">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="56f1d-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="56f1d-284">(30)</span><span class="sxs-lookup"><span data-stu-id="56f1d-284">(30)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-285">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="56f1d-285">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="56f1d-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56f1d-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="56f1d-287">(31)</span><span class="sxs-lookup"><span data-stu-id="56f1d-287">(31)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-288">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-288">Device is not working properly.</span></span> <span data-ttu-id="56f1d-289">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="56f1d-289">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="56f1d-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-291">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="56f1d-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-293">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="56f1d-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-294">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="56f1d-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="56f1d-295">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="56f1d-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-299">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56f1d-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-300">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="56f1d-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="56f1d-301">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="56f1d-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="56f1d-302">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-303">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="56f1d-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-306">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="56f1d-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-307">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="56f1d-307">Textual description of the object.</span></span>

<span data-ttu-id="56f1d-308">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="56f1d-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-312">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56f1d-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-313">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56f1d-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="56f1d-314">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-315">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="56f1d-315">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-316">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="56f1d-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-318">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="56f1d-318">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="56f1d-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-320">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="56f1d-320">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-323">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="56f1d-323">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="56f1d-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-325">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="56f1d-325">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-326">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-328">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria de UPS da DMTF \| 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" porcentagem ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-329">Estimativa percentual do custo total restante de um UPS que usa tecnologia de bateria.</span><span class="sxs-lookup"><span data-stu-id="56f1d-329">Percentage estimate of the remaining full charge for a UPS that uses battery technology.</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-330">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="56f1d-330">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-331">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria de UPS da DMTF \| 1,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-334">O tempo estimado, em minutos, até que a bateria, o gerador ou outra fonte de energia esteja esgotado nas condições de carregamento presentes, caso a energia do utilitário esteja desligada ou seja perdida e permaneça desligada.</span><span class="sxs-lookup"><span data-stu-id="56f1d-334">Estimated time, in minutes, until the battery, generator, or other power source is depleted under the present load conditions if the utility power is off, or is lost and remains off.</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="56f1d-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-336">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="56f1d-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-338">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-339">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-339">Date and time the object was installed.</span></span> <span data-ttu-id="56f1d-340">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="56f1d-341">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-342">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="56f1d-342">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-343">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="56f1d-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-345">Se for **true**, a fonte de alimentação será um suprimento de comutação (em vez de linear).</span><span class="sxs-lookup"><span data-stu-id="56f1d-345">If **TRUE**, the power supply is a switching (rather than linear) supply.</span></span>

<span data-ttu-id="56f1d-346">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-346">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="56f1d-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-348">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-350">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56f1d-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="56f1d-351">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-352">**Nome**</span><span class="sxs-lookup"><span data-stu-id="56f1d-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-355">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="56f1d-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-356">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="56f1d-356">Label by which the object is known.</span></span> <span data-ttu-id="56f1d-357">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="56f1d-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="56f1d-358">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-359">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="56f1d-359">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-362">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="56f1d-362">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-363">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56f1d-363">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="56f1d-364">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="56f1d-365">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="56f1d-365">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-366">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="56f1d-366">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-367">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-367">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-369">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56f1d-369">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="56f1d-370">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="56f1d-370">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="56f1d-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="56f1d-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="56f1d-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="56f1d-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-375">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="56f1d-375">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="56f1d-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-377">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="56f1d-377">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="56f1d-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="56f1d-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-379">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="56f1d-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="56f1d-380">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-380">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="56f1d-381">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="56f1d-381">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="56f1d-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="56f1d-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-383">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="56f1d-383">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="56f1d-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="56f1d-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-385">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="56f1d-385">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-386">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="56f1d-386">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-387">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="56f1d-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-389">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="56f1d-389">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="56f1d-390">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="56f1d-390">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="56f1d-391">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="56f1d-391">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="56f1d-392">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="56f1d-392">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="56f1d-393">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-394">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="56f1d-394">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-395">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-395">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-397">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="56f1d-397">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-398">Frequência, em Hertz, no topo do intervalo de frequência de entrada da fonte de alimentação 1.</span><span class="sxs-lookup"><span data-stu-id="56f1d-398">Frequency, in hertz, at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="56f1d-399">Um valor de 0 (zero) implica em DC.</span><span class="sxs-lookup"><span data-stu-id="56f1d-399">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="56f1d-400">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-400">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-401">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="56f1d-401">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-402">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-403">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-404">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-405">Frequência, em Hertz, no low-end do intervalo de frequência de entrada da fonte de alimentação 1.</span><span class="sxs-lookup"><span data-stu-id="56f1d-405">Frequency, in hertz, at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="56f1d-406">Um valor de 0 (zero) implica em DC.</span><span class="sxs-lookup"><span data-stu-id="56f1d-406">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="56f1d-407">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-407">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-408">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="56f1d-408">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-409">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-411">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivolts")</span><span class="sxs-lookup"><span data-stu-id="56f1d-411">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-412">Se a tensão, em milivolts, ultrapassar o valor especificado pela propriedade **Range1InputVoltageHigh** , o no-break compensará ao cortar a tensão.</span><span class="sxs-lookup"><span data-stu-id="56f1d-412">If the voltage, in millivolts, rises above the value specified by the **Range1InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="56f1d-413">Um valor de 0 (zero) indica que a tensão na qual a corte ocorre é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="56f1d-413">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="56f1d-414">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-414">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-415">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="56f1d-415">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-416">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-418">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivolts")</span><span class="sxs-lookup"><span data-stu-id="56f1d-418">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-419">Se a tensão, em milivolts, cair abaixo do valor especificado pela propriedade **Range1InputVoltageLow** , o no-break compensará aumentando a tensão usando suas fontes de energia.</span><span class="sxs-lookup"><span data-stu-id="56f1d-419">If the voltage, in millivolts, drops below the value specified by the **Range1InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="56f1d-420">Um valor de 0 indica que a tensão em que o aumento ocorre é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="56f1d-420">A value of 0 indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="56f1d-421">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-421">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-422">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="56f1d-422">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-423">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-423">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-424">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-425">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,20 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-426">Frequência, em Hertz, no topo do intervalo de frequência de entrada da fonte de alimentação 2.</span><span class="sxs-lookup"><span data-stu-id="56f1d-426">Frequency, in hertz, at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="56f1d-427">Um valor de 0 (zero) implica em DC.</span><span class="sxs-lookup"><span data-stu-id="56f1d-427">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="56f1d-428">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-428">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-429">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="56f1d-429">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-430">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-431">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-432">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,19 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-433">Frequência, em Hertz, no low-end do intervalo de frequência de entrada da fonte de alimentação 2.</span><span class="sxs-lookup"><span data-stu-id="56f1d-433">Frequency, in hertz, at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="56f1d-434">Um valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="56f1d-434">A value of 0 implies DC.</span></span>

<span data-ttu-id="56f1d-435">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-435">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-436">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="56f1d-436">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-437">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-437">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-439">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivolts")</span><span class="sxs-lookup"><span data-stu-id="56f1d-439">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-440">Se a tensão, em milivolts, ultrapassar o valor especificado pela propriedade **Range2InputVoltageHigh** , o no-break compensará ao cortar a tensão.</span><span class="sxs-lookup"><span data-stu-id="56f1d-440">If the voltage, in millivolts, rises above the value specified by the **Range2InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="56f1d-441">Um valor de 0 (zero) indica que a tensão na qual a corte ocorre é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="56f1d-441">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="56f1d-442">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-442">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-443">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="56f1d-443">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-444">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-444">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-446">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivolts")</span><span class="sxs-lookup"><span data-stu-id="56f1d-446">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-447">Se a tensão, em milivolts, cair abaixo do valor especificado pela propriedade **Range2InputVoltageLow** , o no-break compensará aumentando a tensão usando suas fontes de energia.</span><span class="sxs-lookup"><span data-stu-id="56f1d-447">If the voltage, in millivolts, drops below the value specified by the **Range2InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="56f1d-448">Um valor de 0 (zero) indica que a tensão na qual o aumento ocorre é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="56f1d-448">A value of 0 (zero) indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="56f1d-449">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-449">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-450">**RemainingCapacityStatus**</span><span class="sxs-lookup"><span data-stu-id="56f1d-450">**RemainingCapacityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-451">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-453">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria de UPS da DMTF \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-454">Indicação da capacidade restante nas baterias, no gerador ou em outra fonte do UPS.</span><span class="sxs-lookup"><span data-stu-id="56f1d-454">Indication of the capacity remaining in the UPS's batteries, generator, or other source.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="56f1d-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-457">Os minutos estimados restantes de tempo de execução são maiores que o estado de baixa energia definido no UPS (normalmente, dois minutos).</span><span class="sxs-lookup"><span data-stu-id="56f1d-457">Remaining estimated minutes of run-time is greater than the UPS's defined low-power state (typically, two minutes).</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="56f1d-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-459">Os minutos estimados restantes de tempo de execução são menores ou iguais ao estado de baixa energia definido no UPS.</span><span class="sxs-lookup"><span data-stu-id="56f1d-459">Remaining estimated minutes of run-time is less than or equal to the UPS's defined low-power state.</span></span>

</dd> <dt>

<span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>

<span data-ttu-id="56f1d-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Esgotado** (4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Depleted** (4)</span></span>


</dt> <dd>

<span data-ttu-id="56f1d-461">O no-break não será capaz de sustentar a carga presente quando a energia do utilitário for perdida (incluindo a possibilidade de que a energia do utilitário esteja ausente no momento).</span><span class="sxs-lookup"><span data-stu-id="56f1d-461">The UPS will be unable to sustain the present load when the utility power is lost (including the possibility that the utility power is currently absent).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-462">**Status**</span><span class="sxs-lookup"><span data-stu-id="56f1d-462">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-465">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="56f1d-465">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-466">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="56f1d-466">Current status of the object.</span></span> <span data-ttu-id="56f1d-467">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-467">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="56f1d-468">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="56f1d-468">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="56f1d-469">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="56f1d-469">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="56f1d-470">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="56f1d-470">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="56f1d-471">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="56f1d-471">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-472">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="56f1d-472">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="56f1d-473">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="56f1d-473">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="56f1d-474">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="56f1d-474">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="56f1d-475">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="56f1d-475">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="56f1d-476">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="56f1d-476">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="56f1d-477">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="56f1d-477">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="56f1d-478">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="56f1d-478">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="56f1d-479">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="56f1d-479">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="56f1d-480">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="56f1d-480">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-481">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="56f1d-481">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-482">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-484">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-485">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56f1d-485">State of the logical device.</span></span> <span data-ttu-id="56f1d-486">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="56f1d-486">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="56f1d-487">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="56f1d-488">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-488">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-489">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-489">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="56f1d-490">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-490">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="56f1d-491">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-491">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="56f1d-492">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="56f1d-492">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56f1d-493">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="56f1d-493">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-494">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-496">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56f1d-496">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-497">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-497">Scoping system's creation class name.</span></span>

<span data-ttu-id="56f1d-498">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-498">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-499">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="56f1d-499">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-500">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="56f1d-500">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-501">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-502">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56f1d-502">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-503">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="56f1d-503">Scoping system's name.</span></span>

<span data-ttu-id="56f1d-504">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-504">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-505">**TimeOnBackup**</span><span class="sxs-lookup"><span data-stu-id="56f1d-505">**TimeOnBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-506">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-508">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria de UPS da DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-508">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-509">Tempo decorrido, em segundos, desde a última vez que o no-break mudou para energia, gerador ou outra fonte de alimentação.</span><span class="sxs-lookup"><span data-stu-id="56f1d-509">Elapsed time, in seconds, since the UPS last switched to battery power, generator, or other power source.</span></span> <span data-ttu-id="56f1d-510">Ou, a hora desde que a UPS foi reiniciada pela última vez, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="56f1d-510">Or, the time since the UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="56f1d-511">Se o UPS estiver online, será retornado 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="56f1d-511">If the UPS is online, 0 (zero) will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-512">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="56f1d-512">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-513">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56f1d-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-514">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-515">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,21 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliwatts ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-515">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-516">Potência total de saída da fonte de energia, em miliwatts.</span><span class="sxs-lookup"><span data-stu-id="56f1d-516">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="56f1d-517">Um valor de 0 (zero) denota desconhecido.</span><span class="sxs-lookup"><span data-stu-id="56f1d-517">A value of 0 (zero) denotes unknown.</span></span>

<span data-ttu-id="56f1d-518">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-518">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="56f1d-519">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="56f1d-519">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56f1d-520">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56f1d-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-521">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="56f1d-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56f1d-522">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,16 ")</span><span class="sxs-lookup"><span data-stu-id="56f1d-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="56f1d-523">Tipo de alternância de intervalo de tensão de entrada implementado na fonte de alimentação.</span><span class="sxs-lookup"><span data-stu-id="56f1d-523">Type of input-voltage range switching implemented in the power supply.</span></span>

<span data-ttu-id="56f1d-524">Essa propriedade é herdada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-524">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="56f1d-525">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="56f1d-525">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56f1d-526">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="56f1d-526">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="56f1d-527">**Manual** (3)</span><span class="sxs-lookup"><span data-stu-id="56f1d-527">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="56f1d-528">**Autocomutação** (4)</span><span class="sxs-lookup"><span data-stu-id="56f1d-528">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="56f1d-529">**Faixa ampla** (5)</span><span class="sxs-lookup"><span data-stu-id="56f1d-529">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="56f1d-530">**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="56f1d-530">**Not Applicable** (6)</span></span>


<span data-ttu-id="56f1d-531"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="56f1d-531"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="56f1d-532">Comentários</span><span class="sxs-lookup"><span data-stu-id="56f1d-532">Remarks</span></span>

<span data-ttu-id="56f1d-533">A classe **CIM \_ UninterruptiblePowerSupply** é derivada do [**CIM \_ powersupply**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-533">The **CIM\_UninterruptiblePowerSupply** class is derived from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="56f1d-534">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="56f1d-534">WMI does not implement this class.</span></span> <span data-ttu-id="56f1d-535">Para classes WMI derivadas do **CIM \_ UninterruptiblePowerSupply**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="56f1d-535">For WMI classes derived from **CIM\_UninterruptiblePowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="56f1d-536">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="56f1d-536">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="56f1d-537">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="56f1d-537">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f1d-538">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56f1d-538">Requirements</span></span>



| <span data-ttu-id="56f1d-539">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f1d-539">Requirement</span></span> | <span data-ttu-id="56f1d-540">Valor</span><span class="sxs-lookup"><span data-stu-id="56f1d-540">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56f1d-541">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56f1d-541">Minimum supported client</span></span><br/> | <span data-ttu-id="56f1d-542">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56f1d-542">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56f1d-543">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56f1d-543">Minimum supported server</span></span><br/> | <span data-ttu-id="56f1d-544">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56f1d-544">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56f1d-545">Namespace</span><span class="sxs-lookup"><span data-stu-id="56f1d-545">Namespace</span></span><br/>                | <span data-ttu-id="56f1d-546">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="56f1d-546">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56f1d-547">MOF</span><span class="sxs-lookup"><span data-stu-id="56f1d-547">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56f1d-548"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56f1d-548"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56f1d-549">DLL</span><span class="sxs-lookup"><span data-stu-id="56f1d-549">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56f1d-550"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56f1d-550"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56f1d-551">Confira também</span><span class="sxs-lookup"><span data-stu-id="56f1d-551">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f1d-552">**Fonte de \_ alimentação CIM**</span><span class="sxs-lookup"><span data-stu-id="56f1d-552">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

