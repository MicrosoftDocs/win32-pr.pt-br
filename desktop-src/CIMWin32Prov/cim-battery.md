---
description: A \_ classe de bateria CIM representa os recursos e o gerenciamento do dispositivo lógico da bateria. Essa classe se aplica a baterias em sistemas de laptop e outras baterias internas e externas.
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: Classe CIM_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755242"
---
# <a name="cim_battery-class"></a><span data-ttu-id="31881-104">\_Classe de bateria CIM</span><span class="sxs-lookup"><span data-stu-id="31881-104">CIM\_Battery class</span></span>

<span data-ttu-id="31881-105">A classe de **\_ bateria CIM** representa os recursos e o gerenciamento do dispositivo lógico da bateria.</span><span class="sxs-lookup"><span data-stu-id="31881-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="31881-106">Essa classe se aplica a baterias em sistemas de laptop e outras baterias internas e externas.</span><span class="sxs-lookup"><span data-stu-id="31881-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31881-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="31881-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31881-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31881-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31881-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="31881-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="31881-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="31881-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31881-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31881-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="31881-112">Membros</span><span class="sxs-lookup"><span data-stu-id="31881-112">Members</span></span>

<span data-ttu-id="31881-113">A classe de **\_ bateria CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="31881-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="31881-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="31881-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="31881-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31881-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31881-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="31881-116">Methods</span></span>

<span data-ttu-id="31881-117">A classe de **\_ bateria CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="31881-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="31881-118">Método</span><span class="sxs-lookup"><span data-stu-id="31881-118">Method</span></span>                                                             | <span data-ttu-id="31881-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="31881-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31881-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="31881-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="31881-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="31881-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="31881-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="31881-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="31881-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="31881-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="31881-124">Define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="31881-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="31881-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="31881-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="31881-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31881-126">Properties</span></span>

<span data-ttu-id="31881-127">A classe de **\_ bateria CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="31881-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31881-128">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="31881-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31881-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31881-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="31881-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="31881-132">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31881-132">Availability and status of the device.</span></span>

<span data-ttu-id="31881-133">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31881-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="31881-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31881-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="31881-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="31881-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="31881-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="31881-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="31881-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="31881-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="31881-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="31881-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="31881-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="31881-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="31881-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="31881-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="31881-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="31881-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="31881-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31881-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="31881-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="31881-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="31881-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="31881-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="31881-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="31881-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="31881-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="31881-147">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="31881-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="31881-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="31881-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="31881-149">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="31881-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="31881-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="31881-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="31881-151">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="31881-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="31881-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="31881-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="31881-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="31881-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="31881-154">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="31881-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="31881-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="31881-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="31881-156">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="31881-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="31881-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="31881-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="31881-158">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="31881-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="31881-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="31881-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="31881-160">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="31881-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="31881-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="31881-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="31881-162">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="31881-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="31881-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31881-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31881-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-166">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,14 ")</span><span class="sxs-lookup"><span data-stu-id="31881-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="31881-167">Descrição do status de cobrança da bateria.</span><span class="sxs-lookup"><span data-stu-id="31881-167">Description of the battery's charge status.</span></span> <span data-ttu-id="31881-168">O valor 10 não é válido no esquema CIM, que não representa nenhuma bateria sendo instalada no Desktop Management Interface (DMI).</span><span class="sxs-lookup"><span data-stu-id="31881-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="31881-169">Nesse caso, o objeto não deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="31881-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31881-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="31881-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="31881-171">Outros.</span><span class="sxs-lookup"><span data-stu-id="31881-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31881-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="31881-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="31881-173">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="31881-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="31881-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Totalmente cobrado** (3)</span><span class="sxs-lookup"><span data-stu-id="31881-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31881-175">Totalmente cobrado.</span><span class="sxs-lookup"><span data-stu-id="31881-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="31881-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (4)</span><span class="sxs-lookup"><span data-stu-id="31881-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="31881-177">Baixa:</span><span class="sxs-lookup"><span data-stu-id="31881-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="31881-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="31881-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="31881-179">Crítica.</span><span class="sxs-lookup"><span data-stu-id="31881-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="31881-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Carregando** (6)</span><span class="sxs-lookup"><span data-stu-id="31881-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="31881-181">Carregada.</span><span class="sxs-lookup"><span data-stu-id="31881-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="31881-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Carregando e alto** (7)</span><span class="sxs-lookup"><span data-stu-id="31881-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="31881-183">Carregando e alto.</span><span class="sxs-lookup"><span data-stu-id="31881-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="31881-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Carregando e baixo** (8)</span><span class="sxs-lookup"><span data-stu-id="31881-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="31881-185">Carregando e baixo.</span><span class="sxs-lookup"><span data-stu-id="31881-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="31881-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Cobrança e crítico** (9)</span><span class="sxs-lookup"><span data-stu-id="31881-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="31881-187">Cobrança e crítico.</span><span class="sxs-lookup"><span data-stu-id="31881-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="31881-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (10)</span><span class="sxs-lookup"><span data-stu-id="31881-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="31881-189">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="31881-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="31881-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Parcialmente cobrado** (11)</span><span class="sxs-lookup"><span data-stu-id="31881-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="31881-191">Parcialmente cobrado.</span><span class="sxs-lookup"><span data-stu-id="31881-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-192">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="31881-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-195">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="31881-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="31881-196">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="31881-196">A short textual description of the object.</span></span>

<span data-ttu-id="31881-197">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31881-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-198">**Química**</span><span class="sxs-lookup"><span data-stu-id="31881-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-199">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31881-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31881-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-201">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="31881-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="31881-202">Enumeração que descreve a química da bateria.</span><span class="sxs-lookup"><span data-stu-id="31881-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31881-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="31881-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="31881-204">Outros.</span><span class="sxs-lookup"><span data-stu-id="31881-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31881-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="31881-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="31881-206">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="31881-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="31881-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Liderar Acid** (3)</span><span class="sxs-lookup"><span data-stu-id="31881-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31881-208">Comece a acid.</span><span class="sxs-lookup"><span data-stu-id="31881-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="31881-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Níquel cádmio** (4)</span><span class="sxs-lookup"><span data-stu-id="31881-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="31881-210">Níquel cádmio.</span><span class="sxs-lookup"><span data-stu-id="31881-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="31881-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Hydride de metal de níquel** (5)</span><span class="sxs-lookup"><span data-stu-id="31881-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="31881-212">Hydride de metal de níquel.</span><span class="sxs-lookup"><span data-stu-id="31881-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="31881-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Íon de** lítio (6)</span><span class="sxs-lookup"><span data-stu-id="31881-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="31881-214">Íon de lítio.</span><span class="sxs-lookup"><span data-stu-id="31881-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="31881-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Ar Zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="31881-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="31881-216">Ar Zinc.</span><span class="sxs-lookup"><span data-stu-id="31881-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="31881-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Polymer de lítio** (8)</span><span class="sxs-lookup"><span data-stu-id="31881-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="31881-218">Polymer de lítio.</span><span class="sxs-lookup"><span data-stu-id="31881-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="31881-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-220">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-222">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="31881-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="31881-223">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="31881-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="31881-224">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="31881-225">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="31881-225">**This device is working properly.**</span></span> <span data-ttu-id="31881-226"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="31881-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="31881-227">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="31881-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="31881-228">(1)</span><span class="sxs-lookup"><span data-stu-id="31881-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="31881-229">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="31881-230">(2)</span><span class="sxs-lookup"><span data-stu-id="31881-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="31881-231">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="31881-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="31881-232">(3)</span><span class="sxs-lookup"><span data-stu-id="31881-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="31881-233">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="31881-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="31881-234">(4)</span><span class="sxs-lookup"><span data-stu-id="31881-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="31881-235">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="31881-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="31881-236">(5)</span><span class="sxs-lookup"><span data-stu-id="31881-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="31881-237">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="31881-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="31881-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="31881-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="31881-239">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="31881-239">**Cannot filter.**</span></span> <span data-ttu-id="31881-240">(7)</span><span class="sxs-lookup"><span data-stu-id="31881-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="31881-241">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="31881-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="31881-242">(8)</span><span class="sxs-lookup"><span data-stu-id="31881-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="31881-243">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="31881-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="31881-244">(9)</span><span class="sxs-lookup"><span data-stu-id="31881-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="31881-245">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="31881-245">**This device cannot start.**</span></span> <span data-ttu-id="31881-246">(10)</span><span class="sxs-lookup"><span data-stu-id="31881-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="31881-247">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="31881-247">**This device failed.**</span></span> <span data-ttu-id="31881-248">(11)</span><span class="sxs-lookup"><span data-stu-id="31881-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="31881-249">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="31881-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="31881-250">12</span><span class="sxs-lookup"><span data-stu-id="31881-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="31881-251">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="31881-252">(13)</span><span class="sxs-lookup"><span data-stu-id="31881-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="31881-253">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="31881-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="31881-254">(14)</span><span class="sxs-lookup"><span data-stu-id="31881-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="31881-255">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="31881-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="31881-256">(15)</span><span class="sxs-lookup"><span data-stu-id="31881-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="31881-257">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="31881-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="31881-258">(16)</span><span class="sxs-lookup"><span data-stu-id="31881-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="31881-259">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="31881-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="31881-260">(17)</span><span class="sxs-lookup"><span data-stu-id="31881-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="31881-261">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="31881-262">(18)</span><span class="sxs-lookup"><span data-stu-id="31881-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="31881-263">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="31881-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="31881-264">(19)</span><span class="sxs-lookup"><span data-stu-id="31881-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="31881-265">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="31881-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="31881-266">(20)</span><span class="sxs-lookup"><span data-stu-id="31881-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="31881-267">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="31881-268">(21)</span><span class="sxs-lookup"><span data-stu-id="31881-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="31881-269">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="31881-269">**This device is disabled.**</span></span> <span data-ttu-id="31881-270">(22)</span><span class="sxs-lookup"><span data-stu-id="31881-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="31881-271">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="31881-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="31881-272">(23)</span><span class="sxs-lookup"><span data-stu-id="31881-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="31881-273">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="31881-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="31881-274">(24)</span><span class="sxs-lookup"><span data-stu-id="31881-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="31881-275">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="31881-276">(25)</span><span class="sxs-lookup"><span data-stu-id="31881-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="31881-277">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="31881-278">(26)</span><span class="sxs-lookup"><span data-stu-id="31881-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="31881-279">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="31881-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="31881-280">(27)</span><span class="sxs-lookup"><span data-stu-id="31881-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="31881-281">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="31881-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="31881-282">(28)</span><span class="sxs-lookup"><span data-stu-id="31881-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="31881-283">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="31881-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="31881-284">(29)</span><span class="sxs-lookup"><span data-stu-id="31881-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="31881-285">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="31881-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="31881-286">(30)</span><span class="sxs-lookup"><span data-stu-id="31881-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="31881-287">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="31881-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="31881-288">(31)</span><span class="sxs-lookup"><span data-stu-id="31881-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-289">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="31881-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-290">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="31881-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31881-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-292">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="31881-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="31881-293">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="31881-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="31881-294">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-295">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31881-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-298">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31881-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31881-299">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="31881-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="31881-300">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="31881-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="31881-301">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-302">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="31881-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-305">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="31881-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="31881-306">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="31881-306">A textual description of the object.</span></span>

<span data-ttu-id="31881-307">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31881-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-308">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="31881-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-309">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-311">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-hours ")</span><span class="sxs-lookup"><span data-stu-id="31881-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="31881-312">Capacidade projetada da bateria em milliwatt-horas.</span><span class="sxs-lookup"><span data-stu-id="31881-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="31881-313">Se não houver suporte para essa propriedade, insira 0.</span><span class="sxs-lookup"><span data-stu-id="31881-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="31881-314">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="31881-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-315">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="31881-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="31881-316">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-317">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivolts ")</span><span class="sxs-lookup"><span data-stu-id="31881-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="31881-318">Voltagem projetada da bateria em milivolts.</span><span class="sxs-lookup"><span data-stu-id="31881-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="31881-319">Se não houver suporte para esse atributo, insira 0.</span><span class="sxs-lookup"><span data-stu-id="31881-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="31881-320">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="31881-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="31881-321">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="31881-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-324">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31881-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31881-325">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="31881-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="31881-326">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-327">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="31881-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-328">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="31881-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31881-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31881-330">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="31881-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="31881-331">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="31881-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31881-335">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="31881-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="31881-336">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-337">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="31881-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-338">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31881-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31881-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-340">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span><span class="sxs-lookup"><span data-stu-id="31881-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="31881-341">Porcentagem estimada do custo total restante.</span><span class="sxs-lookup"><span data-stu-id="31881-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="31881-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="31881-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-343">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-345">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="31881-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="31881-346">O tempo estimado, em minutos, até que a carga da bateria fique esgotada nas condições de carregamento presentes, caso a energia do utilitário esteja desligada, seja perdida e permaneça desligada ou se um laptop estiver desconectado de uma fonte de alimentação.</span><span class="sxs-lookup"><span data-stu-id="31881-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="31881-347">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="31881-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-348">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-349">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-350">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="31881-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="31881-351">Tempo de vida esperado da bateria, em minutos, supondo que a bateria está totalmente carregada.</span><span class="sxs-lookup"><span data-stu-id="31881-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="31881-352">Essa propriedade representa a vida útil total esperada da bateria, não sua vida útil atual, que é indicada pela propriedade **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="31881-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="31881-353">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="31881-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-354">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-356">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milliwatt-hours ")</span><span class="sxs-lookup"><span data-stu-id="31881-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="31881-357">A capacidade de carga total da bateria em milliwatt-horas.</span><span class="sxs-lookup"><span data-stu-id="31881-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="31881-358">Compare esse valor com a propriedade **DesignCapacity** para determinar quando a bateria requer substituição.</span><span class="sxs-lookup"><span data-stu-id="31881-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="31881-359">A vida útil de uma bateria é normalmente quando a propriedade **FullChargeCapacity** cai abaixo de 80% da propriedade **DesignCapacity** .</span><span class="sxs-lookup"><span data-stu-id="31881-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="31881-360">Se não houver suporte para essa propriedade, insira 0.</span><span class="sxs-lookup"><span data-stu-id="31881-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="31881-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31881-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-362">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31881-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31881-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-364">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="31881-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="31881-365">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="31881-365">Indicates when the object was installed.</span></span> <span data-ttu-id="31881-366">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="31881-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="31881-367">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31881-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-368">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="31881-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-369">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31881-371">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="31881-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="31881-372">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-373">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="31881-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-374">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-376">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="31881-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="31881-377">Tempo máximo, em minutos, para encarregar totalmente a bateria.</span><span class="sxs-lookup"><span data-stu-id="31881-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="31881-378">Essa propriedade representa o tempo para recarregar uma bateria totalmente descarregada, não o tempo de cobrança restante atual, que é indicado na propriedade **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="31881-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="31881-379">**Nome**</span><span class="sxs-lookup"><span data-stu-id="31881-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-380">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-382">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="31881-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="31881-383">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="31881-383">Label by which the object is known.</span></span> <span data-ttu-id="31881-384">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="31881-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="31881-385">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31881-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="31881-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-389">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="31881-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="31881-390">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="31881-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="31881-391">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="31881-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="31881-392">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="31881-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-394">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31881-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31881-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31881-396">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="31881-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="31881-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31881-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="31881-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="31881-399">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="31881-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="31881-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="31881-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="31881-401">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31881-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="31881-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="31881-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="31881-403">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="31881-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="31881-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="31881-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="31881-405">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="31881-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="31881-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="31881-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="31881-407">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="31881-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="31881-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="31881-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="31881-409">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="31881-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="31881-410">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="31881-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="31881-411">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="31881-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="31881-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="31881-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="31881-413">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="31881-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="31881-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="31881-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="31881-415">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="31881-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-416">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="31881-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-417">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="31881-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31881-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31881-419">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="31881-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="31881-420">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="31881-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="31881-421">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="31881-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="31881-422">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="31881-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="31881-423">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-424">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="31881-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-425">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-426">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-427">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,10 ")</span><span class="sxs-lookup"><span data-stu-id="31881-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="31881-428">Dados de bateria inteligente-número de versão de especificação com suporte nesta bateria.</span><span class="sxs-lookup"><span data-stu-id="31881-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="31881-429">Se a bateria não oferecer suporte a essa função, o valor deverá ser deixado vazio.</span><span class="sxs-lookup"><span data-stu-id="31881-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="31881-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="31881-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-431">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-432">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-433">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="31881-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="31881-434">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="31881-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="31881-435">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="31881-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="31881-436">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="31881-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="31881-437">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="31881-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="31881-438">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="31881-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="31881-439">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="31881-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="31881-440">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="31881-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="31881-441">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="31881-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="31881-442">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="31881-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="31881-443">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="31881-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="31881-444">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="31881-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="31881-445">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="31881-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31881-446">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="31881-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="31881-447">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="31881-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="31881-448">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="31881-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="31881-449">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="31881-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="31881-450">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="31881-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="31881-451">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="31881-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="31881-452">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="31881-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="31881-453">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="31881-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="31881-454">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="31881-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="31881-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-456">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="31881-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31881-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-458">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="31881-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="31881-459">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="31881-459">State of the logical device.</span></span> <span data-ttu-id="31881-460">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="31881-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="31881-461">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="31881-462">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="31881-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="31881-463">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="31881-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="31881-464">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="31881-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="31881-465">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="31881-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="31881-466">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="31881-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="31881-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31881-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-468">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-470">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31881-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31881-471">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="31881-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="31881-472">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="31881-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-474">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="31881-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31881-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-476">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31881-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31881-477">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="31881-477">The scoping system's name.</span></span>

<span data-ttu-id="31881-478">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="31881-479">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="31881-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-480">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-481">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-482">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="31881-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="31881-483">Tempo decorrido, em segundos, desde a última vez em que o UPS do sistema de computador mudou para a energia da bateria ou a quantidade de tempo desde que o sistema ou o UPS foi reiniciado pela última vez, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="31881-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="31881-484">Um valor de 0 será retornado se a bateria estiver "online".</span><span class="sxs-lookup"><span data-stu-id="31881-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="31881-485">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="31881-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31881-486">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31881-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31881-487">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31881-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31881-488">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Bateria portátil DMTF \| 2,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="31881-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="31881-489">Tempo restante, em minutos, para cobrar totalmente a bateria na taxa de carregamento e no uso atual.</span><span class="sxs-lookup"><span data-stu-id="31881-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31881-490">Comentários</span><span class="sxs-lookup"><span data-stu-id="31881-490">Remarks</span></span>

<span data-ttu-id="31881-491">A classe de **\_ bateria CIM** é derivada [**do \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="31881-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="31881-492">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="31881-492">WMI does not implement this class.</span></span> <span data-ttu-id="31881-493">Para obter mais informações sobre classes derivadas **da \_ bateria CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="31881-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="31881-494">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="31881-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31881-495">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="31881-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31881-496">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31881-496">Requirements</span></span>



| <span data-ttu-id="31881-497">Requisito</span><span class="sxs-lookup"><span data-stu-id="31881-497">Requirement</span></span> | <span data-ttu-id="31881-498">Valor</span><span class="sxs-lookup"><span data-stu-id="31881-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31881-499">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31881-499">Minimum supported client</span></span><br/> | <span data-ttu-id="31881-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31881-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31881-501">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31881-501">Minimum supported server</span></span><br/> | <span data-ttu-id="31881-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31881-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31881-503">Namespace</span><span class="sxs-lookup"><span data-stu-id="31881-503">Namespace</span></span><br/>                | <span data-ttu-id="31881-504">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="31881-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31881-505">MOF</span><span class="sxs-lookup"><span data-stu-id="31881-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31881-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31881-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31881-507">DLL</span><span class="sxs-lookup"><span data-stu-id="31881-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31881-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31881-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31881-509">Confira também</span><span class="sxs-lookup"><span data-stu-id="31881-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31881-510">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="31881-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

