---
description: A \_ classe de ventilador CIM representa os recursos e o gerenciamento de um dispositivo de resfriamento de ventilador.
ms.assetid: eddfb694-cba1-45e2-998f-f93355520c80
ms.tgt_platform: multiple
title: Classe CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan
- CIM_Fan.ActiveCooling
- CIM_Fan.Availability
- CIM_Fan.Caption
- CIM_Fan.ConfigManagerErrorCode
- CIM_Fan.ConfigManagerUserConfig
- CIM_Fan.CreationClassName
- CIM_Fan.Description
- CIM_Fan.DesiredSpeed
- CIM_Fan.DeviceID
- CIM_Fan.ErrorCleared
- CIM_Fan.ErrorDescription
- CIM_Fan.InstallDate
- CIM_Fan.LastErrorCode
- CIM_Fan.Name
- CIM_Fan.PNPDeviceID
- CIM_Fan.PowerManagementCapabilities
- CIM_Fan.PowerManagementSupported
- CIM_Fan.Status
- CIM_Fan.StatusInfo
- CIM_Fan.SystemCreationClassName
- CIM_Fan.SystemName
- CIM_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a06e0ddebbdadf7cb4e6dd61afa3fa7c178f661
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826460"
---
# <a name="cim_fan-class"></a><span data-ttu-id="62bb0-103">\_Classe de ventilador CIM</span><span class="sxs-lookup"><span data-stu-id="62bb0-103">CIM\_Fan class</span></span>

<span data-ttu-id="62bb0-104">A classe de **\_ ventilador CIM** representa os recursos e o gerenciamento de um dispositivo de resfriamento de ventilador.</span><span class="sxs-lookup"><span data-stu-id="62bb0-104">The **CIM\_Fan** class represents the capabilities and management of a fan cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62bb0-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="62bb0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62bb0-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="62bb0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62bb0-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="62bb0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="62bb0-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="62bb0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62bb0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62bb0-109">Syntax</span></span>

``` syntax
[UUID("{0A59C856-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Fan : CIM_CoolingDevice
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="62bb0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="62bb0-110">Members</span></span>

<span data-ttu-id="62bb0-111">A classe de **\_ ventilador CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="62bb0-111">The **CIM\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="62bb0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="62bb0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="62bb0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62bb0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="62bb0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="62bb0-114">Methods</span></span>

<span data-ttu-id="62bb0-115">A classe de **\_ ventilador CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="62bb0-115">The **CIM\_Fan** class has these methods.</span></span>



| <span data-ttu-id="62bb0-116">Método</span><span class="sxs-lookup"><span data-stu-id="62bb0-116">Method</span></span>                                                         | <span data-ttu-id="62bb0-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="62bb0-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62bb0-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="62bb0-118">**Reset**</span></span>](reset-method-in-class-cim-fan.md)                 | <span data-ttu-id="62bb0-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62bb0-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="62bb0-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="62bb0-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="62bb0-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="62bb0-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-fan.md) | <span data-ttu-id="62bb0-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="62bb0-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="62bb0-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="62bb0-124">**SETSPEED**</span><span class="sxs-lookup"><span data-stu-id="62bb0-124">**SetSpeed**</span></span>](setspeed-method-in-class-cim-fan.md)           | <span data-ttu-id="62bb0-125">Define a velocidade do ventilador.</span><span class="sxs-lookup"><span data-stu-id="62bb0-125">Sets the fan speed.</span></span> <span data-ttu-id="62bb0-126">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="62bb0-126">Not implemented by WMI.</span></span><br/>                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="62bb0-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62bb0-127">Properties</span></span>

<span data-ttu-id="62bb0-128">A classe de **\_ ventilador CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62bb0-128">The **CIM\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62bb0-129">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="62bb0-129">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-130">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62bb0-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-132">Se **for true**, o dispositivo de resfriamento fornecerá o resfriamento ativo (em oposição ao passivo).</span><span class="sxs-lookup"><span data-stu-id="62bb0-132">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="62bb0-133">Essa propriedade é herdada do [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-133">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-134">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="62bb0-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62bb0-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="62bb0-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-138">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-138">Availability and status of the device.</span></span>

<span data-ttu-id="62bb0-139">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62bb0-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="62bb0-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62bb0-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="62bb0-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="62bb0-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="62bb0-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="62bb0-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="62bb0-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="62bb0-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="62bb0-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="62bb0-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="62bb0-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="62bb0-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="62bb0-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="62bb0-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="62bb0-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="62bb0-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="62bb0-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="62bb0-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="62bb0-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="62bb0-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="62bb0-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="62bb0-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="62bb0-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="62bb0-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="62bb0-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-153">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="62bb0-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="62bb0-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="62bb0-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-155">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="62bb0-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="62bb0-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-157">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="62bb0-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="62bb0-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="62bb0-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="62bb0-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="62bb0-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-160">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="62bb0-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="62bb0-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="62bb0-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-162">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="62bb0-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="62bb0-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="62bb0-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-164">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="62bb0-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="62bb0-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="62bb0-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-166">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="62bb0-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="62bb0-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-168">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="62bb0-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62bb0-169">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="62bb0-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="62bb0-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-173">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="62bb0-173">Short textual description of the object.</span></span>

<span data-ttu-id="62bb0-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="62bb0-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62bb0-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-178">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62bb0-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-179">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="62bb0-179">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="62bb0-180">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="62bb0-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="62bb0-182"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="62bb0-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-183">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="62bb0-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="62bb0-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="62bb0-185">(1)</span><span class="sxs-lookup"><span data-stu-id="62bb0-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-186">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="62bb0-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62bb0-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="62bb0-188">(2)</span><span class="sxs-lookup"><span data-stu-id="62bb0-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="62bb0-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="62bb0-190">(3)</span><span class="sxs-lookup"><span data-stu-id="62bb0-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-191">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="62bb0-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="62bb0-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="62bb0-193">(4)</span><span class="sxs-lookup"><span data-stu-id="62bb0-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-194">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="62bb0-194">Device is not working properly.</span></span> <span data-ttu-id="62bb0-195">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="62bb0-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="62bb0-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="62bb0-197">(5)</span><span class="sxs-lookup"><span data-stu-id="62bb0-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-198">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="62bb0-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="62bb0-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="62bb0-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="62bb0-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-201">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="62bb0-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="62bb0-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="62bb0-203">(7)</span><span class="sxs-lookup"><span data-stu-id="62bb0-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="62bb0-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="62bb0-205">(8)</span><span class="sxs-lookup"><span data-stu-id="62bb0-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-206">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="62bb0-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="62bb0-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="62bb0-208">(9)</span><span class="sxs-lookup"><span data-stu-id="62bb0-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-209">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="62bb0-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="62bb0-211">(10)</span><span class="sxs-lookup"><span data-stu-id="62bb0-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-212">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="62bb0-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="62bb0-214">(11)</span><span class="sxs-lookup"><span data-stu-id="62bb0-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-215">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="62bb0-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="62bb0-217">12</span><span class="sxs-lookup"><span data-stu-id="62bb0-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-218">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="62bb0-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="62bb0-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="62bb0-220">(13)</span><span class="sxs-lookup"><span data-stu-id="62bb0-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-221">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="62bb0-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="62bb0-223">(14)</span><span class="sxs-lookup"><span data-stu-id="62bb0-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-224">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="62bb0-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="62bb0-226">(15)</span><span class="sxs-lookup"><span data-stu-id="62bb0-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-227">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="62bb0-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="62bb0-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="62bb0-229">(16)</span><span class="sxs-lookup"><span data-stu-id="62bb0-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-230">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="62bb0-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="62bb0-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="62bb0-232">(17)</span><span class="sxs-lookup"><span data-stu-id="62bb0-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-233">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="62bb0-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62bb0-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="62bb0-235">(18)</span><span class="sxs-lookup"><span data-stu-id="62bb0-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-236">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="62bb0-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="62bb0-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="62bb0-238">(19)</span><span class="sxs-lookup"><span data-stu-id="62bb0-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="62bb0-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="62bb0-240">(20)</span><span class="sxs-lookup"><span data-stu-id="62bb0-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-241">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="62bb0-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="62bb0-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="62bb0-243">(21)</span><span class="sxs-lookup"><span data-stu-id="62bb0-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-244">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="62bb0-244">System failure.</span></span> <span data-ttu-id="62bb0-245">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="62bb0-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="62bb0-246">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="62bb0-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="62bb0-248">(22)</span><span class="sxs-lookup"><span data-stu-id="62bb0-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-249">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="62bb0-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="62bb0-251">(23)</span><span class="sxs-lookup"><span data-stu-id="62bb0-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-252">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="62bb0-252">System failure.</span></span> <span data-ttu-id="62bb0-253">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="62bb0-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="62bb0-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="62bb0-255">(24)</span><span class="sxs-lookup"><span data-stu-id="62bb0-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-256">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="62bb0-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="62bb0-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="62bb0-258">(25)</span><span class="sxs-lookup"><span data-stu-id="62bb0-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="62bb0-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="62bb0-261">(26)</span><span class="sxs-lookup"><span data-stu-id="62bb0-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-262">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="62bb0-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="62bb0-264">(27)</span><span class="sxs-lookup"><span data-stu-id="62bb0-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-265">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="62bb0-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="62bb0-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="62bb0-267">(28)</span><span class="sxs-lookup"><span data-stu-id="62bb0-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-268">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="62bb0-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="62bb0-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="62bb0-270">(29)</span><span class="sxs-lookup"><span data-stu-id="62bb0-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-271">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="62bb0-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="62bb0-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="62bb0-273">(30)</span><span class="sxs-lookup"><span data-stu-id="62bb0-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-274">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="62bb0-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62bb0-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="62bb0-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="62bb0-276">(31)</span><span class="sxs-lookup"><span data-stu-id="62bb0-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-277">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="62bb0-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62bb0-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="62bb0-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-279">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62bb0-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-281">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62bb0-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-282">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="62bb0-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="62bb0-283">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62bb0-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-285">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-287">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62bb0-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-288">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="62bb0-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="62bb0-289">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="62bb0-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="62bb0-290">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-291">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62bb0-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-292">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-294">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="62bb0-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-295">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="62bb0-295">Textual description of the object.</span></span>

<span data-ttu-id="62bb0-296">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-297">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="62bb0-297">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-298">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62bb0-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-300">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("rotações por minuto")</span><span class="sxs-lookup"><span data-stu-id="62bb0-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-301">Velocidade de ventilador solicitada, definida em rotações por minuto, quando há suporte para um ventilador de velocidade variável.</span><span class="sxs-lookup"><span data-stu-id="62bb0-301">Requested fan speed, defined in revolutions per minute, when a variable speed fan is supported.</span></span> <span data-ttu-id="62bb0-302">A velocidade atual é determinada por um sensor ([**\_ tacômetro do CIM**](cim-tachometer.md)) que está associado ao ventilador usando a relação de [**\_ AssociatedSensor do CIM**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="62bb0-302">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="62bb0-303">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="62bb0-303">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-304">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="62bb0-304">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-305">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-307">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62bb0-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-308">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62bb0-308">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="62bb0-309">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="62bb0-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-311">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62bb0-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-313">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="62bb0-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="62bb0-314">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="62bb0-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-318">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="62bb0-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="62bb0-319">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-320">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62bb0-320">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-321">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62bb0-321">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-323">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="62bb0-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-324">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-324">Date and time the object was installed.</span></span> <span data-ttu-id="62bb0-325">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-325">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="62bb0-326">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-327">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="62bb0-327">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-328">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62bb0-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-330">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62bb0-330">Last error code reported by the logical device.</span></span>

<span data-ttu-id="62bb0-331">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-332">**Nome**</span><span class="sxs-lookup"><span data-stu-id="62bb0-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-335">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="62bb0-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-336">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="62bb0-336">Label by which the object is known.</span></span> <span data-ttu-id="62bb0-337">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="62bb0-337">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="62bb0-338">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="62bb0-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-342">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62bb0-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-343">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62bb0-343">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="62bb0-344">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="62bb0-345">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="62bb0-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="62bb0-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-347">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62bb0-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-349">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62bb0-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="62bb0-350">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="62bb0-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62bb0-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="62bb0-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="62bb0-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="62bb0-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-353">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-353">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="62bb0-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="62bb0-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="62bb0-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="62bb0-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-356">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="62bb0-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="62bb0-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="62bb0-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-358">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="62bb0-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="62bb0-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="62bb0-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-360">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="62bb0-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="62bb0-361">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="62bb0-362">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="62bb0-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="62bb0-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="62bb0-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-364">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="62bb0-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="62bb0-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="62bb0-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="62bb0-366">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="62bb0-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62bb0-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="62bb0-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-368">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62bb0-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-369">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-370">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="62bb0-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="62bb0-371">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="62bb0-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="62bb0-372">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="62bb0-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="62bb0-373">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="62bb0-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="62bb0-374">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-375">**Status**</span><span class="sxs-lookup"><span data-stu-id="62bb0-375">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-376">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-377">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-378">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="62bb0-378">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-379">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="62bb0-379">Current status of the object.</span></span> <span data-ttu-id="62bb0-380">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="62bb0-381">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="62bb0-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="62bb0-382">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="62bb0-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="62bb0-383">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="62bb0-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="62bb0-384">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="62bb0-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62bb0-385">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="62bb0-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="62bb0-386">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="62bb0-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="62bb0-387">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="62bb0-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="62bb0-388">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="62bb0-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="62bb0-389">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="62bb0-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="62bb0-390">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="62bb0-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="62bb0-391">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="62bb0-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="62bb0-392">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="62bb0-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="62bb0-393">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="62bb0-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62bb0-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="62bb0-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-395">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62bb0-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-397">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="62bb0-397">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-398">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="62bb0-398">State of the logical device.</span></span> <span data-ttu-id="62bb0-399">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="62bb0-399">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="62bb0-400">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62bb0-401">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="62bb0-401">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62bb0-402">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="62bb0-402">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="62bb0-403">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="62bb0-403">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="62bb0-404">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="62bb0-404">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="62bb0-405">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="62bb0-405">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62bb0-406">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62bb0-406">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-407">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-409">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62bb0-409">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-410">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-410">Scoping system's creation class name.</span></span>

<span data-ttu-id="62bb0-411">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-412">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="62bb0-412">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-413">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62bb0-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-415">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62bb0-415">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-416">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="62bb0-416">Scoping system's name.</span></span>

<span data-ttu-id="62bb0-417">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62bb0-418">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="62bb0-418">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62bb0-419">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62bb0-419">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62bb0-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62bb0-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62bb0-421">Se **for true**, o ventilador dará suporte a velocidades de variáveis.</span><span class="sxs-lookup"><span data-stu-id="62bb0-421">If **TRUE**, the fan supports variable speeds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62bb0-422">Comentários</span><span class="sxs-lookup"><span data-stu-id="62bb0-422">Remarks</span></span>

<span data-ttu-id="62bb0-423">A classe de **\_ ventilador CIM** é derivada do [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-423">The **CIM\_Fan** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="62bb0-424">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="62bb0-424">WMI does not implement this class.</span></span> <span data-ttu-id="62bb0-425">Para classes derivadas do **\_ ventilador CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="62bb0-425">For classes derived from **CIM\_Fan**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="62bb0-426">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="62bb0-426">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62bb0-427">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="62bb0-427">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62bb0-428">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62bb0-428">Requirements</span></span>



| <span data-ttu-id="62bb0-429">Requisito</span><span class="sxs-lookup"><span data-stu-id="62bb0-429">Requirement</span></span> | <span data-ttu-id="62bb0-430">Valor</span><span class="sxs-lookup"><span data-stu-id="62bb0-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62bb0-431">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62bb0-431">Minimum supported client</span></span><br/> | <span data-ttu-id="62bb0-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62bb0-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62bb0-433">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62bb0-433">Minimum supported server</span></span><br/> | <span data-ttu-id="62bb0-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62bb0-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62bb0-435">Namespace</span><span class="sxs-lookup"><span data-stu-id="62bb0-435">Namespace</span></span><br/>                | <span data-ttu-id="62bb0-436">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="62bb0-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62bb0-437">MOF</span><span class="sxs-lookup"><span data-stu-id="62bb0-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62bb0-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62bb0-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62bb0-439">DLL</span><span class="sxs-lookup"><span data-stu-id="62bb0-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62bb0-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62bb0-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62bb0-441">Confira também</span><span class="sxs-lookup"><span data-stu-id="62bb0-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62bb0-442">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="62bb0-442">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

