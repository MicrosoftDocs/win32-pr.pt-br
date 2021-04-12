---
description: A \_ classe CIM DiscreteSensor tem um conjunto de valores de cadeia de caracteres legais que ele pode relatar. Os valores são enumerados na propriedade PossibleValues do sensor. Um sensor discreto sempre tem uma leitura atual que corresponde a um dos valores enumerados.
ms.assetid: 58ab5b4d-ff8b-4981-8f09-c9a255635110
ms.tgt_platform: multiple
title: Classe CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor
- CIM_DiscreteSensor.AcceptableValues
- CIM_DiscreteSensor.Availability
- CIM_DiscreteSensor.Caption
- CIM_DiscreteSensor.ConfigManagerErrorCode
- CIM_DiscreteSensor.ConfigManagerUserConfig
- CIM_DiscreteSensor.CreationClassName
- CIM_DiscreteSensor.CurrentReading
- CIM_DiscreteSensor.Description
- CIM_DiscreteSensor.DeviceID
- CIM_DiscreteSensor.ErrorCleared
- CIM_DiscreteSensor.ErrorDescription
- CIM_DiscreteSensor.InstallDate
- CIM_DiscreteSensor.LastErrorCode
- CIM_DiscreteSensor.Name
- CIM_DiscreteSensor.PNPDeviceID
- CIM_DiscreteSensor.PossibleValues
- CIM_DiscreteSensor.PowerManagementCapabilities
- CIM_DiscreteSensor.PowerManagementSupported
- CIM_DiscreteSensor.Status
- CIM_DiscreteSensor.StatusInfo
- CIM_DiscreteSensor.SystemCreationClassName
- CIM_DiscreteSensor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5211aa8d840384eaf140c1afbeb2fa9c0680cb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501007"
---
# <a name="cim_discretesensor-class"></a><span data-ttu-id="0b488-105">\_Classe CIM DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="0b488-105">CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="0b488-106">A classe **CIM \_ DiscreteSensor** tem um conjunto de valores de cadeia de caracteres legais que ele pode relatar.</span><span class="sxs-lookup"><span data-stu-id="0b488-106">The **CIM\_DiscreteSensor** class has a set of legal string values that it can report.</span></span> <span data-ttu-id="0b488-107">Os valores são enumerados na propriedade **PossibleValues** do sensor.</span><span class="sxs-lookup"><span data-stu-id="0b488-107">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="0b488-108">Um sensor discreto sempre tem uma leitura atual que corresponde a um dos valores enumerados.</span><span class="sxs-lookup"><span data-stu-id="0b488-108">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

<span data-ttu-id="0b488-109">Devido à adição das propriedades **CurrentState** e **PossibleStates** ao [**\_ sensor CIM**](cim-sensor.md), a subclasse de sensor discreto não é mais necessária; no entanto, ela é mantida para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="0b488-109">Given the addition of the **CurrentState** and **PossibleStates** properties to [**CIM\_Sensor**](cim-sensor.md), the discrete sensor subclass is no longer necessary; however, it is retained for backward compatibility.</span></span> <span data-ttu-id="0b488-110">As informações nas propriedades **CurrentReading** e **PossibleValues** normalmente têm os mesmos valores e semânticas das propriedades **CurrentState** e **PossibleStates** , que são herdadas do **\_ sensor CIM**.</span><span class="sxs-lookup"><span data-stu-id="0b488-110">Information in the **CurrentReading** and **PossibleValues** properties typically has the same values and semantics as for the **CurrentState** and **PossibleStates** properties, which are inherited from **CIM\_Sensor**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b488-111">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0b488-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b488-112">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b488-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b488-113">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b488-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0b488-114">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0b488-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b488-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b488-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{1BF00330-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DiscreteSensor : CIM_Sensor
{
  string   AcceptableValues[];
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  string   PossibleValues[];
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="0b488-116">Membros</span><span class="sxs-lookup"><span data-stu-id="0b488-116">Members</span></span>

<span data-ttu-id="0b488-117">A classe **CIM \_ DiscreteSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b488-117">The **CIM\_DiscreteSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="0b488-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b488-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b488-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b488-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b488-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b488-120">Methods</span></span>

<span data-ttu-id="0b488-121">A classe **CIM \_ DiscreteSensor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0b488-121">The **CIM\_DiscreteSensor** class has these methods.</span></span>



| <span data-ttu-id="0b488-122">Método</span><span class="sxs-lookup"><span data-stu-id="0b488-122">Method</span></span>                                                                | <span data-ttu-id="0b488-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b488-123">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b488-124">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="0b488-124">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="0b488-125">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b488-125">Requests a reset of the logical device.</span></span> <span data-ttu-id="0b488-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0b488-126">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0b488-127">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0b488-127">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="0b488-128">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="0b488-128">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0b488-129">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0b488-129">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0b488-130">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b488-130">Properties</span></span>

<span data-ttu-id="0b488-131">A classe **CIM \_ DiscreteSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b488-131">The **CIM\_DiscreteSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b488-132">**AcceptableValues**</span><span class="sxs-lookup"><span data-stu-id="0b488-132">**AcceptableValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-133">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b488-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-135">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0b488-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-136">As cadeias de caracteres na propriedade **PossibleValues** são consideradas aceitáveis (ou seja, não são erros).</span><span class="sxs-lookup"><span data-stu-id="0b488-136">Strings in the **PossibleValues** property are considered acceptable (that is, they are not errors).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-137">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="0b488-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b488-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="0b488-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-141">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-141">Availability and status of the device.</span></span>

<span data-ttu-id="0b488-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0b488-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0b488-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b488-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0b488-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0b488-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="0b488-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0b488-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="0b488-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0b488-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="0b488-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0b488-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="0b488-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0b488-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="0b488-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0b488-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="0b488-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0b488-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="0b488-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0b488-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="0b488-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0b488-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="0b488-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0b488-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="0b488-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0b488-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="0b488-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-156">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0b488-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0b488-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="0b488-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-158">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="0b488-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0b488-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="0b488-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-160">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="0b488-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0b488-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="0b488-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0b488-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="0b488-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-163">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0b488-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0b488-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="0b488-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-165">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0b488-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0b488-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="0b488-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-167">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="0b488-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0b488-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="0b488-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-169">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="0b488-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0b488-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="0b488-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-171">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="0b488-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0b488-172">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0b488-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-175">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0b488-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-176">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0b488-176">Short textual description of the object.</span></span>

<span data-ttu-id="0b488-177">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0b488-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-179">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b488-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-181">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0b488-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-182">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0b488-182">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0b488-183">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0b488-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0b488-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0b488-185"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="0b488-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-186">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0b488-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0b488-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="0b488-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0b488-188">(1)</span><span class="sxs-lookup"><span data-stu-id="0b488-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-189">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="0b488-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0b488-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0b488-191">(2)</span><span class="sxs-lookup"><span data-stu-id="0b488-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0b488-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="0b488-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0b488-193">(3)</span><span class="sxs-lookup"><span data-stu-id="0b488-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-194">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="0b488-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0b488-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0b488-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0b488-196">(4)</span><span class="sxs-lookup"><span data-stu-id="0b488-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-197">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="0b488-197">Device is not working properly.</span></span> <span data-ttu-id="0b488-198">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0b488-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0b488-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="0b488-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0b488-200">(5)</span><span class="sxs-lookup"><span data-stu-id="0b488-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-201">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="0b488-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0b488-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="0b488-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0b488-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="0b488-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-204">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0b488-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0b488-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="0b488-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0b488-206">(7)</span><span class="sxs-lookup"><span data-stu-id="0b488-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0b488-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="0b488-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0b488-208">(8)</span><span class="sxs-lookup"><span data-stu-id="0b488-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-209">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="0b488-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0b488-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="0b488-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0b488-211">(9)</span><span class="sxs-lookup"><span data-stu-id="0b488-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-212">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0b488-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="0b488-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0b488-214">(10)</span><span class="sxs-lookup"><span data-stu-id="0b488-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-215">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0b488-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="0b488-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0b488-217">(11)</span><span class="sxs-lookup"><span data-stu-id="0b488-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-218">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0b488-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="0b488-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0b488-220">12</span><span class="sxs-lookup"><span data-stu-id="0b488-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-221">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="0b488-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0b488-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0b488-223">(13)</span><span class="sxs-lookup"><span data-stu-id="0b488-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-224">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0b488-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="0b488-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0b488-226">(14)</span><span class="sxs-lookup"><span data-stu-id="0b488-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-227">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="0b488-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0b488-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="0b488-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0b488-229">(15)</span><span class="sxs-lookup"><span data-stu-id="0b488-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-230">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="0b488-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0b488-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="0b488-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0b488-232">(16)</span><span class="sxs-lookup"><span data-stu-id="0b488-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-233">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="0b488-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0b488-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="0b488-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0b488-235">(17)</span><span class="sxs-lookup"><span data-stu-id="0b488-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-236">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0b488-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0b488-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0b488-238">(18)</span><span class="sxs-lookup"><span data-stu-id="0b488-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-239">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="0b488-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0b488-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="0b488-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0b488-241">(19)</span><span class="sxs-lookup"><span data-stu-id="0b488-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0b488-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="0b488-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0b488-243">(20)</span><span class="sxs-lookup"><span data-stu-id="0b488-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-244">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="0b488-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0b488-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0b488-246">(21)</span><span class="sxs-lookup"><span data-stu-id="0b488-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-247">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0b488-247">System failure.</span></span> <span data-ttu-id="0b488-248">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0b488-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0b488-249">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0b488-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="0b488-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0b488-251">(22)</span><span class="sxs-lookup"><span data-stu-id="0b488-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-252">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="0b488-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0b488-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="0b488-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0b488-254">(23)</span><span class="sxs-lookup"><span data-stu-id="0b488-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-255">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="0b488-255">System failure.</span></span> <span data-ttu-id="0b488-256">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="0b488-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0b488-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="0b488-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0b488-258">(24)</span><span class="sxs-lookup"><span data-stu-id="0b488-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-259">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="0b488-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0b488-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0b488-261">(25)</span><span class="sxs-lookup"><span data-stu-id="0b488-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-262">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0b488-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0b488-264">(26)</span><span class="sxs-lookup"><span data-stu-id="0b488-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-265">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b488-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0b488-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="0b488-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0b488-267">(27)</span><span class="sxs-lookup"><span data-stu-id="0b488-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-268">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="0b488-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0b488-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="0b488-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0b488-270">(28)</span><span class="sxs-lookup"><span data-stu-id="0b488-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-271">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="0b488-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0b488-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="0b488-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0b488-273">(29)</span><span class="sxs-lookup"><span data-stu-id="0b488-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-274">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="0b488-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0b488-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="0b488-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0b488-276">(30)</span><span class="sxs-lookup"><span data-stu-id="0b488-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-277">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="0b488-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0b488-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="0b488-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0b488-279">(31)</span><span class="sxs-lookup"><span data-stu-id="0b488-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-280">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="0b488-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0b488-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0b488-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-282">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b488-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-284">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0b488-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-285">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0b488-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0b488-286">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b488-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-290">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0b488-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-291">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0b488-291">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="0b488-292">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0b488-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0b488-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="0b488-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-297">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0b488-297">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-298">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="0b488-298">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="0b488-299">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0b488-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-300">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-302">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0b488-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-303">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0b488-303">Textual description of the object.</span></span>

<span data-ttu-id="0b488-304">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0b488-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-308">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0b488-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-309">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b488-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0b488-310">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0b488-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-312">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b488-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b488-314">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="0b488-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0b488-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0b488-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b488-319">Cadeia de caracteres de forma livre que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="0b488-319">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0b488-320">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0b488-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-322">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0b488-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-324">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0b488-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-325">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="0b488-325">Date and time when the object was installed.</span></span> <span data-ttu-id="0b488-326">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="0b488-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0b488-327">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0b488-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-329">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b488-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b488-331">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b488-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0b488-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-333">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0b488-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-336">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="0b488-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-337">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="0b488-337">Label by which the object is known.</span></span> <span data-ttu-id="0b488-338">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="0b488-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0b488-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0b488-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-341">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-343">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0b488-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-344">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b488-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="0b488-345">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0b488-346">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0b488-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0b488-347">**PossibleValues**</span><span class="sxs-lookup"><span data-stu-id="0b488-347">**PossibleValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-348">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b488-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-350">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0b488-350">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-351">Enumera as saídas de cadeia de caracteres do sensor discreto.</span><span class="sxs-lookup"><span data-stu-id="0b488-351">Enumerates the string outputs from the discrete sensor.</span></span>

</dd> <dt>

<span data-ttu-id="0b488-352">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0b488-352">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-353">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b488-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0b488-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b488-355">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b488-355">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0b488-356">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="0b488-356">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b488-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0b488-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0b488-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="0b488-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0b488-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0b488-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0b488-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0b488-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-361">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0b488-361">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0b488-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="0b488-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-363">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="0b488-363">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0b488-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="0b488-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-365">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="0b488-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0b488-366">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="0b488-366">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0b488-367">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0b488-367">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0b488-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="0b488-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-369">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="0b488-369">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0b488-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="0b488-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0b488-371">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="0b488-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0b488-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0b488-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-373">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0b488-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b488-375">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="0b488-375">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0b488-376">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0b488-376">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0b488-377">Essa propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento ou, se habilitado, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="0b488-377">This property does not indicate that power management features are currently enabled, or if enabled, what features are supported.</span></span> <span data-ttu-id="0b488-378">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="0b488-378">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0b488-379">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-380">**Status**</span><span class="sxs-lookup"><span data-stu-id="0b488-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-383">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0b488-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-384">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0b488-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="0b488-385">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="0b488-385">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0b488-386">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="0b488-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0b488-387">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="0b488-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0b488-388">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="0b488-388">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0b488-389">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="0b488-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0b488-390">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="0b488-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0b488-391">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0b488-392">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0b488-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0b488-393">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0b488-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0b488-394">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0b488-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0b488-395">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0b488-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b488-396">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0b488-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0b488-397">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0b488-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0b488-398">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0b488-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0b488-399">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0b488-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0b488-400">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0b488-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0b488-401">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0b488-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0b488-402">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0b488-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0b488-403">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0b488-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0b488-404">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0b488-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b488-405">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0b488-405">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-406">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b488-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-408">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="0b488-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0b488-409">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b488-409">State of the logical device.</span></span> <span data-ttu-id="0b488-410">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="0b488-410">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0b488-411">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0b488-412">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="0b488-412">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0b488-413">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="0b488-413">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0b488-414">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0b488-414">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0b488-415">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="0b488-415">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0b488-416">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="0b488-416">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b488-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0b488-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-418">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-420">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0b488-420">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-421">Propriedade **CreationClassName** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0b488-421">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="0b488-422">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-422">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b488-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0b488-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b488-424">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b488-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b488-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b488-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b488-426">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0b488-426">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0b488-427">Propriedade de **nome** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0b488-427">Scoping system's **Name** property.</span></span>

<span data-ttu-id="0b488-428">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b488-429">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b488-429">Remarks</span></span>

<span data-ttu-id="0b488-430">A classe **CIM \_ DiscreteSensor** é derivada do [**\_ sensor CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="0b488-430">The **CIM\_DiscreteSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="0b488-431">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0b488-431">WMI does not implement this class.</span></span>

<span data-ttu-id="0b488-432">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b488-432">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b488-433">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0b488-433">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b488-434">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b488-434">Requirements</span></span>



| <span data-ttu-id="0b488-435">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b488-435">Requirement</span></span> | <span data-ttu-id="0b488-436">Valor</span><span class="sxs-lookup"><span data-stu-id="0b488-436">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b488-437">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b488-437">Minimum supported client</span></span><br/> | <span data-ttu-id="0b488-438">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b488-438">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b488-439">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b488-439">Minimum supported server</span></span><br/> | <span data-ttu-id="0b488-440">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b488-440">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b488-441">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b488-441">Namespace</span></span><br/>                | <span data-ttu-id="0b488-442">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0b488-442">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b488-443">MOF</span><span class="sxs-lookup"><span data-stu-id="0b488-443">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b488-444"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b488-444"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b488-445">DLL</span><span class="sxs-lookup"><span data-stu-id="0b488-445">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b488-446"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b488-446"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b488-447">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b488-447">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b488-448">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="0b488-448">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

