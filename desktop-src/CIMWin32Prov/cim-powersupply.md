---
description: A \_ classe CIM PowerSupply representa os recursos e o gerenciamento do dispositivo lógico da fonte de energia.
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: Classe CIM_PowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164002"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="b1ee7-103">\_Classe de POWERSUPPLY CIM</span><span class="sxs-lookup"><span data-stu-id="b1ee7-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="b1ee7-104">A classe **CIM \_ powersupply** representa os recursos e o gerenciamento do dispositivo lógico da fonte de energia.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1ee7-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b1ee7-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b1ee7-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b1ee7-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ee7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1ee7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="b1ee7-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b1ee7-110">Members</span></span>

<span data-ttu-id="b1ee7-111">A classe de **\_ powersupply CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1ee7-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="b1ee7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1ee7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1ee7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1ee7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1ee7-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1ee7-114">Methods</span></span>

<span data-ttu-id="b1ee7-115">A classe de **\_ powersupply CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="b1ee7-116">Método</span><span class="sxs-lookup"><span data-stu-id="b1ee7-116">Method</span></span>                                                                 | <span data-ttu-id="b1ee7-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1ee7-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1ee7-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="b1ee7-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b1ee7-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b1ee7-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="b1ee7-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b1ee7-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1ee7-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1ee7-124">Properties</span></span>

<span data-ttu-id="b1ee7-125">A classe de **\_ powersupply CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1ee7-126">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,15 ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-130">Intervalo de tensão que está em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="b1ee7-131">Se o fornecimento não estiver atualmente desenhando energia, o valor 6 ("nenhum") poderá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="b1ee7-132">Essas informações são necessárias no caso de uma fonte de alimentação ininterrupta (UPS), uma subclasse de **\_ powersupply CIM**.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1ee7-133">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ee7-134">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="b1ee7-135">**Intervalo 1** (3)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="b1ee7-136">**Intervalo 2** (4)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="b1ee7-137">**Ambos** (5)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="b1ee7-138">**Nenhum** (6)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ee7-139">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-142">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-143">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-143">Availability and status of the device.</span></span>

<span data-ttu-id="b1ee7-144">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1ee7-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ee7-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b1ee7-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-148">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="b1ee7-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b1ee7-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b1ee7-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1ee7-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b1ee7-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="b1ee7-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b1ee7-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b1ee7-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1ee7-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b1ee7-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b1ee7-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b1ee7-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-159">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b1ee7-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-161">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b1ee7-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-163">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b1ee7-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b1ee7-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-166">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b1ee7-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-168">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b1ee7-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-170">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b1ee7-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-172">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b1ee7-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-174">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ee7-175">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-178">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-179">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-179">Short textual description of the object.</span></span>

<span data-ttu-id="b1ee7-180">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-182">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-184">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-185">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b1ee7-186">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b1ee7-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b1ee7-188"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-189">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b1ee7-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b1ee7-191">(1)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-192">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1ee7-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b1ee7-194">(2)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b1ee7-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b1ee7-196">(3)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-197">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1ee7-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b1ee7-199">(4)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-200">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-200">Device is not working properly.</span></span> <span data-ttu-id="b1ee7-201">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b1ee7-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b1ee7-203">(5)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-204">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b1ee7-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b1ee7-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-207">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b1ee7-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b1ee7-209">(7)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b1ee7-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b1ee7-211">(8)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-212">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b1ee7-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b1ee7-214">(9)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-215">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-215">Device is not working properly.</span></span> <span data-ttu-id="b1ee7-216">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b1ee7-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b1ee7-218">(10)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-219">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b1ee7-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b1ee7-221">(11)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-222">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b1ee7-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b1ee7-224">12</span><span class="sxs-lookup"><span data-stu-id="b1ee7-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-225">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b1ee7-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b1ee7-227">(13)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-228">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b1ee7-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b1ee7-230">(14)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-231">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b1ee7-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b1ee7-233">(15)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-234">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b1ee7-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b1ee7-236">(16)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-237">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b1ee7-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b1ee7-239">(17)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-240">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1ee7-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b1ee7-242">(18)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-243">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b1ee7-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b1ee7-245">(19)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1ee7-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b1ee7-247">(20)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-248">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b1ee7-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b1ee7-250">(21)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-251">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-251">System failure.</span></span> <span data-ttu-id="b1ee7-252">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b1ee7-253">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b1ee7-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b1ee7-255">(22)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-256">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b1ee7-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b1ee7-258">(23)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-259">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-259">System failure.</span></span> <span data-ttu-id="b1ee7-260">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b1ee7-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b1ee7-262">(24)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-263">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1ee7-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1ee7-265">(25)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-266">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1ee7-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1ee7-268">(26)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-269">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b1ee7-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b1ee7-271">(27)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-272">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b1ee7-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b1ee7-274">(28)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-275">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b1ee7-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b1ee7-277">(29)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-278">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b1ee7-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b1ee7-280">(30)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-281">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1ee7-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b1ee7-283">(31)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-284">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-284">Device is not working properly.</span></span> <span data-ttu-id="b1ee7-285">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ee7-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-287">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-289">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-290">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b1ee7-291">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-295">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-296">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b1ee7-297">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b1ee7-298">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-299">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-302">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-303">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-303">Textual description of the object.</span></span>

<span data-ttu-id="b1ee7-304">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-308">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-309">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b1ee7-310">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-314">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b1ee7-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-319">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b1ee7-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-322">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-324">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-325">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-325">Date and time the object was installed.</span></span> <span data-ttu-id="b1ee7-326">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b1ee7-327">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-328">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-329">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-331">Se for **true**, a fonte de alimentação será um suprimento de comutação (versus linear).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-332">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-333">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-335">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b1ee7-336">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-337">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-340">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-341">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-341">Label by which the object is known.</span></span> <span data-ttu-id="b1ee7-342">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b1ee7-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-345">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-346">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-347">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-348">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b1ee7-349">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1ee7-350">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b1ee7-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-352">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-354">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b1ee7-355">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ee7-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b1ee7-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1ee7-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1ee7-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-360">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b1ee7-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-362">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b1ee7-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-364">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b1ee7-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b1ee7-365">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b1ee7-366">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b1ee7-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-368">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b1ee7-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b1ee7-370">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ee7-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-372">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-374">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b1ee7-375">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b1ee7-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b1ee7-376">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b1ee7-377">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b1ee7-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b1ee7-378">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-380">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-382">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-383">Frequência (em Hertz) no topo do intervalo de frequência de entrada da fonte de alimentação 1.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="b1ee7-384">Um valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-386">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-388">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-389">Frequência (em Hertz) no low-end do intervalo de frequência de entrada da fonte de alimentação 1.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="b1ee7-390">Um valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-392">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-395">Alta tensão do intervalo de tensão de entrada 1 para a fonte de alimentação, em milivolts.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="b1ee7-396">O valor 0 denota "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="b1ee7-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-398">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-400">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-401">Baixa voltagem do intervalo de voltagem de entrada 1 para a fonte de alimentação, em milivolts.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="b1ee7-402">O valor 0 denota "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="b1ee7-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-404">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-406">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,20 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-407">Frequência (em Hertz) no topo do intervalo de frequência de entrada da fonte de alimentação 2.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="b1ee7-408">Um valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-410">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-412">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,19 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-413">Frequência (em Hertz) no low-end do intervalo de frequência de entrada da fonte de alimentação 2.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="b1ee7-414">Um valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-416">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-418">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-419">Alta tensão do intervalo de tensão de entrada 2 para a fonte de alimentação, em milivolts.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="b1ee7-420">O valor 0 denota "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="b1ee7-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-422">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-424">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-425">Baixa voltagem do intervalo de tensão de entrada 2 para essa fonte de alimentação, em milivolts.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="b1ee7-426">O valor 0 denota "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="b1ee7-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-427">**Status**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-430">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-431">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-431">Current status of the object.</span></span>

<span data-ttu-id="b1ee7-432">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b1ee7-433">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b1ee7-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1ee7-434">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1ee7-435">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1ee7-436">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ee7-437">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1ee7-438">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1ee7-439">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1ee7-440">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1ee7-441">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1ee7-442">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1ee7-443">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1ee7-444">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1ee7-445">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ee7-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-447">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-448">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-449">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-450">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-450">State of the logical device.</span></span> <span data-ttu-id="b1ee7-451">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b1ee7-452">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1ee7-453">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ee7-454">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1ee7-455">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1ee7-456">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1ee7-457">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1ee7-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-459">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-460">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-461">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-462">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="b1ee7-463">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-465">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-467">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-468">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-468">Scoping system's name.</span></span>

<span data-ttu-id="b1ee7-469">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-470">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-471">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-473">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,21 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliwatts ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-474">Potência total de saída da fonte de energia, em miliwatts.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="b1ee7-475">O valor 0 denota "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="b1ee7-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="b1ee7-476">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1ee7-477">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1ee7-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1ee7-479">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fonte de energia DMTF \| 2,16 ")</span><span class="sxs-lookup"><span data-stu-id="b1ee7-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="b1ee7-480">Tipo de alternância de intervalo de tensão de entrada implementada na fonte de alimentação.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1ee7-481">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1ee7-482">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="b1ee7-483">**Manual** (3)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="b1ee7-484">**Autocomutação** (4)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="b1ee7-485">**Faixa ampla** (5)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1ee7-486">**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="b1ee7-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="b1ee7-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b1ee7-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b1ee7-488">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1ee7-488">Remarks</span></span>

<span data-ttu-id="b1ee7-489">A classe de **\_ powersupply CIM** é derivada de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1ee7-490">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-490">WMI does not implement this class.</span></span> <span data-ttu-id="b1ee7-491">Para a classe WMI derivada do **CIM \_ powersupply**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b1ee7-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b1ee7-492">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b1ee7-493">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b1ee7-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1ee7-494">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1ee7-494">Requirements</span></span>



| <span data-ttu-id="b1ee7-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ee7-495">Requirement</span></span> | <span data-ttu-id="b1ee7-496">Valor</span><span class="sxs-lookup"><span data-stu-id="b1ee7-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ee7-497">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1ee7-497">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ee7-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1ee7-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1ee7-499">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1ee7-499">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ee7-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1ee7-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1ee7-501">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1ee7-501">Namespace</span></span><br/>                | <span data-ttu-id="b1ee7-502">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b1ee7-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1ee7-503">MOF</span><span class="sxs-lookup"><span data-stu-id="b1ee7-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1ee7-504"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1ee7-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1ee7-505">DLL</span><span class="sxs-lookup"><span data-stu-id="b1ee7-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1ee7-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1ee7-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ee7-507">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1ee7-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ee7-508">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="b1ee7-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

