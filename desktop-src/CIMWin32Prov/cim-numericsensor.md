---
description: A \_ classe CIM NumericSensor representa um sensor numérico que retorna leituras numéricas e, opcionalmente, dá suporte a configurações de limites.
ms.assetid: 9be9ee28-24ee-49d1-871f-73b504c77518
ms.tgt_platform: multiple
title: Classe CIM_NumericSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NumericSensor
- CIM_NumericSensor.Accuracy
- CIM_NumericSensor.Availability
- CIM_NumericSensor.Caption
- CIM_NumericSensor.ConfigManagerErrorCode
- CIM_NumericSensor.ConfigManagerUserConfig
- CIM_NumericSensor.CreationClassName
- CIM_NumericSensor.CurrentReading
- CIM_NumericSensor.Description
- CIM_NumericSensor.DeviceID
- CIM_NumericSensor.ErrorCleared
- CIM_NumericSensor.ErrorDescription
- CIM_NumericSensor.InstallDate
- CIM_NumericSensor.IsLinear
- CIM_NumericSensor.LastErrorCode
- CIM_NumericSensor.LowerThresholdCritical
- CIM_NumericSensor.LowerThresholdFatal
- CIM_NumericSensor.LowerThresholdNonCritical
- CIM_NumericSensor.MaxReadable
- CIM_NumericSensor.MinReadable
- CIM_NumericSensor.Name
- CIM_NumericSensor.NominalReading
- CIM_NumericSensor.NormalMax
- CIM_NumericSensor.NormalMin
- CIM_NumericSensor.PNPDeviceID
- CIM_NumericSensor.PowerManagementCapabilities
- CIM_NumericSensor.PowerManagementSupported
- CIM_NumericSensor.Resolution
- CIM_NumericSensor.Status
- CIM_NumericSensor.StatusInfo
- CIM_NumericSensor.SystemCreationClassName
- CIM_NumericSensor.SystemName
- CIM_NumericSensor.Tolerance
- CIM_NumericSensor.UpperThresholdCritical
- CIM_NumericSensor.UpperThresholdFatal
- CIM_NumericSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2888b56e39184b05484cacd587be140b94dc732e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755847"
---
# <a name="cim_numericsensor-class"></a><span data-ttu-id="93249-103">\_Classe CIM NumericSensor</span><span class="sxs-lookup"><span data-stu-id="93249-103">CIM\_NumericSensor class</span></span>

<span data-ttu-id="93249-104">A classe **CIM \_ NumericSensor** representa um sensor numérico que retorna leituras numéricas e, opcionalmente, dá suporte a configurações de limites.</span><span class="sxs-lookup"><span data-stu-id="93249-104">The **CIM\_NumericSensor** class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93249-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="93249-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="93249-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="93249-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="93249-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="93249-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="93249-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="93249-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93249-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93249-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979C-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_NumericSensor : CIM_Sensor
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

## <a name="members"></a><span data-ttu-id="93249-110">Membros</span><span class="sxs-lookup"><span data-stu-id="93249-110">Members</span></span>

<span data-ttu-id="93249-111">A classe **CIM \_ NumericSensor** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="93249-111">The **CIM\_NumericSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="93249-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="93249-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="93249-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93249-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93249-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="93249-114">Methods</span></span>

<span data-ttu-id="93249-115">A classe **CIM \_ NumericSensor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="93249-115">The **CIM\_NumericSensor** class has these methods.</span></span>



| <span data-ttu-id="93249-116">Método</span><span class="sxs-lookup"><span data-stu-id="93249-116">Method</span></span>                                                                   | <span data-ttu-id="93249-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="93249-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93249-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="93249-118">**Reset**</span></span>](reset-method-in-class-cim-numericsensor.md)                 | <span data-ttu-id="93249-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93249-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="93249-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="93249-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="93249-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="93249-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-numericsensor.md) | <span data-ttu-id="93249-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="93249-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="93249-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="93249-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="93249-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93249-124">Properties</span></span>

<span data-ttu-id="93249-125">A classe **CIM \_ NumericSensor** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="93249-125">The **CIM\_NumericSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93249-126">**Correta**</span><span class="sxs-lookup"><span data-stu-id="93249-126">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-127">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-129">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("centésimos de porcentagem")</span><span class="sxs-lookup"><span data-stu-id="93249-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="93249-130">Precisão do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="93249-130">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="93249-131">Seu valor é registrado como mais ou menos centésimos de uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="93249-131">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="93249-132">Essa propriedade e as propriedades de **resolução** e **tolerância** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="93249-132">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="93249-133">A precisão pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="93249-133">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="93249-134">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="93249-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93249-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93249-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="93249-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="93249-138">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-138">Availability and status of the device.</span></span>

<span data-ttu-id="93249-139">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93249-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93249-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93249-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93249-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="93249-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="93249-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="93249-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="93249-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="93249-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="93249-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="93249-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="93249-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="93249-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="93249-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="93249-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="93249-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="93249-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="93249-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="93249-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="93249-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="93249-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="93249-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="93249-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="93249-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="93249-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="93249-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="93249-153">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="93249-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="93249-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="93249-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="93249-155">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="93249-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="93249-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="93249-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="93249-157">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="93249-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="93249-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="93249-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="93249-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="93249-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="93249-160">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="93249-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="93249-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="93249-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="93249-162">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="93249-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="93249-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="93249-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="93249-164">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="93249-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="93249-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="93249-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="93249-166">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="93249-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="93249-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="93249-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="93249-168">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="93249-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93249-169">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="93249-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="93249-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="93249-173">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="93249-173">Short textual description of the object.</span></span>

<span data-ttu-id="93249-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93249-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="93249-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93249-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-178">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93249-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93249-179">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="93249-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="93249-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="93249-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="93249-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="93249-182"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="93249-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="93249-183">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="93249-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="93249-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="93249-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="93249-185">(1)</span><span class="sxs-lookup"><span data-stu-id="93249-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="93249-186">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="93249-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="93249-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="93249-188">(2)</span><span class="sxs-lookup"><span data-stu-id="93249-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="93249-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="93249-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="93249-190">(3)</span><span class="sxs-lookup"><span data-stu-id="93249-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="93249-191">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="93249-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="93249-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="93249-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="93249-193">(4)</span><span class="sxs-lookup"><span data-stu-id="93249-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="93249-194">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="93249-194">Device is not working properly.</span></span> <span data-ttu-id="93249-195">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="93249-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="93249-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="93249-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="93249-197">(5)</span><span class="sxs-lookup"><span data-stu-id="93249-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="93249-198">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="93249-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="93249-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="93249-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="93249-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="93249-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="93249-201">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="93249-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="93249-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="93249-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="93249-203">(7)</span><span class="sxs-lookup"><span data-stu-id="93249-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="93249-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="93249-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="93249-205">(8)</span><span class="sxs-lookup"><span data-stu-id="93249-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="93249-206">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="93249-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="93249-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="93249-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="93249-208">(9)</span><span class="sxs-lookup"><span data-stu-id="93249-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="93249-209">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="93249-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="93249-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="93249-211">(10)</span><span class="sxs-lookup"><span data-stu-id="93249-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="93249-212">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="93249-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="93249-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="93249-214">(11)</span><span class="sxs-lookup"><span data-stu-id="93249-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="93249-215">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="93249-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="93249-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="93249-217">12</span><span class="sxs-lookup"><span data-stu-id="93249-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="93249-218">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="93249-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="93249-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="93249-220">(13)</span><span class="sxs-lookup"><span data-stu-id="93249-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="93249-221">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="93249-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="93249-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="93249-223">(14)</span><span class="sxs-lookup"><span data-stu-id="93249-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="93249-224">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="93249-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="93249-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="93249-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="93249-226">(15)</span><span class="sxs-lookup"><span data-stu-id="93249-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="93249-227">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="93249-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="93249-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="93249-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="93249-229">(16)</span><span class="sxs-lookup"><span data-stu-id="93249-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="93249-230">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="93249-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="93249-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="93249-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="93249-232">(17)</span><span class="sxs-lookup"><span data-stu-id="93249-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="93249-233">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="93249-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="93249-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="93249-235">(18)</span><span class="sxs-lookup"><span data-stu-id="93249-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="93249-236">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="93249-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="93249-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="93249-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="93249-238">(19)</span><span class="sxs-lookup"><span data-stu-id="93249-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="93249-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="93249-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="93249-240">(20)</span><span class="sxs-lookup"><span data-stu-id="93249-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="93249-241">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="93249-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="93249-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="93249-243">(21)</span><span class="sxs-lookup"><span data-stu-id="93249-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="93249-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="93249-244">System failure.</span></span> <span data-ttu-id="93249-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="93249-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="93249-246">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="93249-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="93249-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="93249-248">(22)</span><span class="sxs-lookup"><span data-stu-id="93249-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="93249-249">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="93249-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="93249-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="93249-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="93249-251">(23)</span><span class="sxs-lookup"><span data-stu-id="93249-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="93249-252">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="93249-252">System failure.</span></span> <span data-ttu-id="93249-253">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="93249-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="93249-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="93249-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="93249-255">(24)</span><span class="sxs-lookup"><span data-stu-id="93249-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="93249-256">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="93249-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="93249-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="93249-258">(25)</span><span class="sxs-lookup"><span data-stu-id="93249-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="93249-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="93249-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="93249-261">(26)</span><span class="sxs-lookup"><span data-stu-id="93249-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="93249-262">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="93249-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="93249-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="93249-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="93249-264">(27)</span><span class="sxs-lookup"><span data-stu-id="93249-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="93249-265">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="93249-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="93249-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="93249-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="93249-267">(28)</span><span class="sxs-lookup"><span data-stu-id="93249-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="93249-268">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="93249-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="93249-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="93249-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="93249-270">(29)</span><span class="sxs-lookup"><span data-stu-id="93249-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="93249-271">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="93249-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="93249-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="93249-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="93249-273">(30)</span><span class="sxs-lookup"><span data-stu-id="93249-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="93249-274">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="93249-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="93249-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="93249-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="93249-276">(31)</span><span class="sxs-lookup"><span data-stu-id="93249-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="93249-277">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="93249-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93249-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="93249-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-279">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93249-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93249-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-281">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93249-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93249-282">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="93249-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="93249-283">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93249-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-287">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93249-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93249-288">Classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="93249-288">Class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="93249-289">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="93249-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="93249-290">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-291">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="93249-291">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-292">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-292">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-294">Valor atual indicado pelo sensor.</span><span class="sxs-lookup"><span data-stu-id="93249-294">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="93249-295">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="93249-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-298">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="93249-298">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="93249-299">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="93249-299">Textual description of the object.</span></span>

<span data-ttu-id="93249-300">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93249-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-301">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="93249-301">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-304">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93249-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93249-305">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93249-305">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="93249-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-307">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="93249-307">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-308">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93249-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93249-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-310">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="93249-310">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="93249-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-312">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="93249-312">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-315">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="93249-315">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="93249-316">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93249-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-318">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93249-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93249-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-320">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="93249-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="93249-321">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="93249-321">Date and time the object was installed.</span></span> <span data-ttu-id="93249-322">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="93249-322">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="93249-323">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93249-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-324">**Islinear**</span><span class="sxs-lookup"><span data-stu-id="93249-324">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-325">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93249-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93249-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-327">Se **for true**, o sensor será linear sobre seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="93249-327">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="93249-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="93249-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-329">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93249-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-331">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93249-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="93249-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-333">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="93249-333">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-334">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-334">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-336">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="93249-336">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="93249-337">Se a propriedade **CurrentReading** estiver entre **LowerThresholdCritical** e **LowerThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="93249-337">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="93249-338">Essa propriedade é herdada **de \_ NumericSensor de CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-338">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="93249-339">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="93249-339">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-340">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-342">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="93249-342">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="93249-343">Se a propriedade **CurrentReading** estiver abaixo de **LowerThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="93249-343">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="93249-344">Essa propriedade é herdada **de \_ NumericSensor de CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-344">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="93249-345">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="93249-345">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-346">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-348">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="93249-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="93249-349">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="93249-349">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="93249-350">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **LowerThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="93249-350">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="93249-351">Essa propriedade é herdada **de \_ NumericSensor de CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-351">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="93249-352">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="93249-352">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-353">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-355">Maior valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="93249-355">Largest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="93249-356">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="93249-356">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-357">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-359">Menor valor da propriedade medida que pode ser lido pelo sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="93249-359">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="93249-360">**Nome**</span><span class="sxs-lookup"><span data-stu-id="93249-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-363">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="93249-363">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="93249-364">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="93249-364">Label by which the object is known.</span></span> <span data-ttu-id="93249-365">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="93249-365">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="93249-366">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93249-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-367">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="93249-367">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-368">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-370">Valor esperado ou "normal" para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="93249-370">Expected or "normal" value for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="93249-371">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="93249-371">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-372">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-372">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-374">Intervalo máximo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="93249-374">Normal maximum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="93249-375">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="93249-375">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-376">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-376">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-378">Intervalo mínimo normal para o sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="93249-378">Normal minimum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="93249-379">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="93249-379">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-380">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-382">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="93249-382">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="93249-383">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93249-383">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="93249-384">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="93249-385">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="93249-385">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="93249-386">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="93249-386">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-387">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93249-387">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93249-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-389">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93249-389">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="93249-390">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-390">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93249-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="93249-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="93249-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="93249-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="93249-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="93249-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="93249-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="93249-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93249-395">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="93249-395">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="93249-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="93249-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93249-397">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="93249-397">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="93249-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="93249-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="93249-399">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="93249-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="93249-400">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="93249-400">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="93249-401">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="93249-401">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="93249-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="93249-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="93249-403">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="93249-403">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="93249-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="93249-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="93249-405">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="93249-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93249-406">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="93249-406">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-407">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93249-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93249-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-409">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="93249-409">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="93249-410">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="93249-410">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="93249-411">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="93249-411">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="93249-412">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="93249-412">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="93249-413">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-414">**Resolução**</span><span class="sxs-lookup"><span data-stu-id="93249-414">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-415">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93249-415">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-417">Capacidade do sensor de resolver diferenças na propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="93249-417">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="93249-418">Esse valor pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="93249-418">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="93249-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="93249-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-422">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="93249-422">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="93249-423">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="93249-423">Current status of the object.</span></span>

<span data-ttu-id="93249-424">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="93249-424">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="93249-425">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="93249-425">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="93249-426">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="93249-426">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="93249-427">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="93249-427">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="93249-428">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="93249-428">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93249-429">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="93249-429">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="93249-430">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="93249-430">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="93249-431">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="93249-431">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="93249-432">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="93249-432">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="93249-433">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="93249-433">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="93249-434">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="93249-434">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="93249-435">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="93249-435">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="93249-436">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="93249-436">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="93249-437">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="93249-437">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93249-438">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="93249-438">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-439">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93249-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93249-440">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-441">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="93249-441">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="93249-442">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93249-442">State of the logical device.</span></span> <span data-ttu-id="93249-443">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="93249-443">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="93249-444">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="93249-445">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="93249-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="93249-446">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="93249-446">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="93249-447">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="93249-447">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="93249-448">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="93249-448">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="93249-449">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="93249-449">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93249-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93249-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-451">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-452">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-453">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93249-453">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93249-454">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="93249-454">Scoping system's creation class name.</span></span>

<span data-ttu-id="93249-455">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-455">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-456">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="93249-456">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-457">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93249-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93249-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93249-459">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93249-459">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93249-460">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="93249-460">Scoping system's name.</span></span>

<span data-ttu-id="93249-461">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="93249-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="93249-462">**Tolerável**</span><span class="sxs-lookup"><span data-stu-id="93249-462">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-463">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-463">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-465">Tolerância do sensor para a propriedade medida.</span><span class="sxs-lookup"><span data-stu-id="93249-465">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="93249-466">Essa propriedade e as propriedades de **resolução** e **precisão** são usadas para calcular o valor real da propriedade física medida.</span><span class="sxs-lookup"><span data-stu-id="93249-466">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="93249-467">A tolerância pode variar dependendo se o dispositivo é linear em seu intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="93249-467">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="93249-468">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="93249-468">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-469">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-469">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-471">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="93249-471">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="93249-472">Se a propriedade **CurrentReading** estiver entre **UpperThresholdCritical** e **UpperThresholdFatal**, o estado atual será crítico.</span><span class="sxs-lookup"><span data-stu-id="93249-472">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="93249-473">Essa propriedade é herdada **de \_ NumericSensor de CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-473">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="93249-474">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="93249-474">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-475">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-475">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-477">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="93249-477">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="93249-478">Se a propriedade **CurrentReading** estiver acima de **UpperThresholdFatal**, o estado atual será fatal.</span><span class="sxs-lookup"><span data-stu-id="93249-478">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="93249-479">Essa propriedade é herdada **de \_ NumericSensor de CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-479">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="93249-480">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="93249-480">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93249-481">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="93249-481">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="93249-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93249-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93249-483">Valor de limite que especifica os intervalos (valores mínimos e máximos) para determinar se o sensor está operando em condições normais, não críticas, críticas ou fatais.</span><span class="sxs-lookup"><span data-stu-id="93249-483">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="93249-484">Se a propriedade **CurrentReading** estiver entre **LowerThresholdNonCritical** e **UpperThresholdNonCritical**, o sensor estará relatando um valor normal.</span><span class="sxs-lookup"><span data-stu-id="93249-484">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="93249-485">Se a propriedade **CurrentReading** estiver entre **UpperThresholdNonCritical** e **UpperThresholdCritical**, o estado atual será não crítico.</span><span class="sxs-lookup"><span data-stu-id="93249-485">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="93249-486">Essa propriedade é herdada **de \_ NumericSensor de CIM**.</span><span class="sxs-lookup"><span data-stu-id="93249-486">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93249-487">Comentários</span><span class="sxs-lookup"><span data-stu-id="93249-487">Remarks</span></span>

<span data-ttu-id="93249-488">A classe **CIM \_ NumericSensor** é derivada do [**\_ sensor CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="93249-488">The **CIM\_NumericSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="93249-489">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="93249-489">WMI does not implement this class.</span></span> <span data-ttu-id="93249-490">Para classes derivadas de **\_ NumericSensor do CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="93249-490">For classes derived from **CIM\_NumericSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="93249-491">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="93249-491">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="93249-492">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="93249-492">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="93249-493">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93249-493">Requirements</span></span>



| <span data-ttu-id="93249-494">Requisito</span><span class="sxs-lookup"><span data-stu-id="93249-494">Requirement</span></span> | <span data-ttu-id="93249-495">Valor</span><span class="sxs-lookup"><span data-stu-id="93249-495">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93249-496">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93249-496">Minimum supported client</span></span><br/> | <span data-ttu-id="93249-497">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93249-497">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93249-498">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93249-498">Minimum supported server</span></span><br/> | <span data-ttu-id="93249-499">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93249-499">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93249-500">Namespace</span><span class="sxs-lookup"><span data-stu-id="93249-500">Namespace</span></span><br/>                | <span data-ttu-id="93249-501">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="93249-501">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93249-502">MOF</span><span class="sxs-lookup"><span data-stu-id="93249-502">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93249-503"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93249-503"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93249-504">DLL</span><span class="sxs-lookup"><span data-stu-id="93249-504">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93249-505"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93249-505"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93249-506">Confira também</span><span class="sxs-lookup"><span data-stu-id="93249-506">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93249-507">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="93249-507">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

