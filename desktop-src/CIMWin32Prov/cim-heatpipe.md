---
description: A \_ classe CIM HeatPipe representa os recursos e o gerenciamento de um dispositivo de resfriamento de tubo de calor.
ms.assetid: 55cbf645-12d8-4f17-a894-43195d42de0e
ms.tgt_platform: multiple
title: Classe CIM_HeatPipe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HeatPipe
- CIM_HeatPipe.ActiveCooling
- CIM_HeatPipe.Availability
- CIM_HeatPipe.Caption
- CIM_HeatPipe.ConfigManagerErrorCode
- CIM_HeatPipe.ConfigManagerUserConfig
- CIM_HeatPipe.CreationClassName
- CIM_HeatPipe.Description
- CIM_HeatPipe.DeviceID
- CIM_HeatPipe.ErrorCleared
- CIM_HeatPipe.ErrorDescription
- CIM_HeatPipe.InstallDate
- CIM_HeatPipe.LastErrorCode
- CIM_HeatPipe.Name
- CIM_HeatPipe.PNPDeviceID
- CIM_HeatPipe.PowerManagementCapabilities
- CIM_HeatPipe.PowerManagementSupported
- CIM_HeatPipe.Status
- CIM_HeatPipe.StatusInfo
- CIM_HeatPipe.SystemCreationClassName
- CIM_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9502509e5a48f4d2f407fddbb6b57766b5f7bffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296095"
---
# <a name="cim_heatpipe-class"></a><span data-ttu-id="cc60f-103">\_Classe CIM HeatPipe</span><span class="sxs-lookup"><span data-stu-id="cc60f-103">CIM\_HeatPipe class</span></span>

<span data-ttu-id="cc60f-104">A classe **CIM \_ HeatPipe** representa os recursos e o gerenciamento de um dispositivo de resfriamento de tubo de calor.</span><span class="sxs-lookup"><span data-stu-id="cc60f-104">The **CIM\_HeatPipe** class represents the capabilities and management of a heat pipe cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc60f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cc60f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cc60f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cc60f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cc60f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cc60f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cc60f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cc60f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc60f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc60f-109">Syntax</span></span>

``` syntax
[UUID("{FE5D55E0-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_HeatPipe : CIM_CoolingDevice
{
  boolean  ActiveCooling;
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
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="cc60f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="cc60f-110">Members</span></span>

<span data-ttu-id="cc60f-111">A classe **CIM \_ HeatPipe** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cc60f-111">The **CIM\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="cc60f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc60f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cc60f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc60f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cc60f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc60f-114">Methods</span></span>

<span data-ttu-id="cc60f-115">A classe **CIM \_ HeatPipe** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cc60f-115">The **CIM\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="cc60f-116">Método</span><span class="sxs-lookup"><span data-stu-id="cc60f-116">Method</span></span>                                                              | <span data-ttu-id="cc60f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc60f-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc60f-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="cc60f-118">**Reset**</span></span>](reset-method-in-class-cim-heatpipe.md)                 | <span data-ttu-id="cc60f-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc60f-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="cc60f-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="cc60f-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="cc60f-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cc60f-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-heatpipe.md) | <span data-ttu-id="cc60f-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="cc60f-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="cc60f-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cc60f-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc60f-124">Properties</span></span>

<span data-ttu-id="cc60f-125">A classe **CIM \_ HeatPipe** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cc60f-125">The **CIM\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc60f-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="cc60f-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-127">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cc60f-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-129">Se **for true**, o dispositivo de resfriamento fornecerá o resfriamento ativo (em oposição ao passivo).</span><span class="sxs-lookup"><span data-stu-id="cc60f-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="cc60f-130">Essa propriedade é herdada do [**CIM \_ CoolingDevice**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-130">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-131">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="cc60f-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-132">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc60f-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-134">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="cc60f-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-135">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-135">Availability and status of the device.</span></span>

<span data-ttu-id="cc60f-136">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cc60f-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cc60f-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc60f-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="cc60f-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cc60f-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="cc60f-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cc60f-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="cc60f-140"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cc60f-141"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="cc60f-141"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cc60f-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="cc60f-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cc60f-143"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="cc60f-143"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cc60f-144"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="cc60f-144"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cc60f-145"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="cc60f-145"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cc60f-146"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="cc60f-146"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cc60f-147"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="cc60f-147"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cc60f-148"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="cc60f-148"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cc60f-149"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="cc60f-149"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-150">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="cc60f-150">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cc60f-151"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="cc60f-151"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-152">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-152">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cc60f-153"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="cc60f-153"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-154">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="cc60f-154">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cc60f-155"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="cc60f-155"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cc60f-156"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="cc60f-156"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-157">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="cc60f-157">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cc60f-158"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="cc60f-158"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-159">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="cc60f-159">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cc60f-160"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="cc60f-160"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-161">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="cc60f-161">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cc60f-162"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="cc60f-162"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-163">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-163">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cc60f-164"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="cc60f-164"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-165">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="cc60f-165">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cc60f-166">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cc60f-166">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-169">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cc60f-169">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-170">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc60f-170">Short textual description of the object.</span></span>

<span data-ttu-id="cc60f-171">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-171">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-172">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cc60f-172">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-173">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc60f-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-175">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cc60f-175">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-176">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cc60f-176">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="cc60f-177">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-177">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cc60f-178"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-178"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="cc60f-179"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="cc60f-179">(0)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-180">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="cc60f-180">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cc60f-181"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-181"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="cc60f-182">(1)</span><span class="sxs-lookup"><span data-stu-id="cc60f-182">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-183">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="cc60f-183">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cc60f-184"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-184"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cc60f-185">(2)</span><span class="sxs-lookup"><span data-stu-id="cc60f-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cc60f-186"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-186"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cc60f-187">(3)</span><span class="sxs-lookup"><span data-stu-id="cc60f-187">(3)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-188">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="cc60f-188">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cc60f-189"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-189"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cc60f-190">(4)</span><span class="sxs-lookup"><span data-stu-id="cc60f-190">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-191">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="cc60f-191">Device is not working properly.</span></span> <span data-ttu-id="cc60f-192">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="cc60f-192">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cc60f-193"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-193"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cc60f-194">(5)</span><span class="sxs-lookup"><span data-stu-id="cc60f-194">(5)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-195">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="cc60f-195">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cc60f-196"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-196"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cc60f-197"> (6)</span><span class="sxs-lookup"><span data-stu-id="cc60f-197">(6)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-198">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc60f-198">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cc60f-199"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-199"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="cc60f-200">(7)</span><span class="sxs-lookup"><span data-stu-id="cc60f-200">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cc60f-201"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-201"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cc60f-202">(8)</span><span class="sxs-lookup"><span data-stu-id="cc60f-202">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-203">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="cc60f-203">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cc60f-204"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-204"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cc60f-205">(9)</span><span class="sxs-lookup"><span data-stu-id="cc60f-205">(9)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-206">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-206">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cc60f-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="cc60f-208">(10)</span><span class="sxs-lookup"><span data-stu-id="cc60f-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-209">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cc60f-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="cc60f-211">(11)</span><span class="sxs-lookup"><span data-stu-id="cc60f-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-212">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cc60f-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cc60f-214">12</span><span class="sxs-lookup"><span data-stu-id="cc60f-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-215">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="cc60f-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cc60f-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cc60f-217">(13)</span><span class="sxs-lookup"><span data-stu-id="cc60f-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-218">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cc60f-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cc60f-220">(14)</span><span class="sxs-lookup"><span data-stu-id="cc60f-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-221">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cc60f-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cc60f-223">(15)</span><span class="sxs-lookup"><span data-stu-id="cc60f-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-224">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="cc60f-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cc60f-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cc60f-226">(16)</span><span class="sxs-lookup"><span data-stu-id="cc60f-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-227">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="cc60f-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cc60f-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cc60f-229">(17)</span><span class="sxs-lookup"><span data-stu-id="cc60f-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-230">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="cc60f-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cc60f-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cc60f-232">(18)</span><span class="sxs-lookup"><span data-stu-id="cc60f-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-233">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="cc60f-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cc60f-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="cc60f-235">(19)</span><span class="sxs-lookup"><span data-stu-id="cc60f-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cc60f-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="cc60f-237">(20)</span><span class="sxs-lookup"><span data-stu-id="cc60f-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-238">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="cc60f-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cc60f-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cc60f-240">(21)</span><span class="sxs-lookup"><span data-stu-id="cc60f-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-241">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="cc60f-241">System failure.</span></span> <span data-ttu-id="cc60f-242">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="cc60f-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="cc60f-243">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cc60f-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="cc60f-245">(22)</span><span class="sxs-lookup"><span data-stu-id="cc60f-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-246">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cc60f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cc60f-248">(23)</span><span class="sxs-lookup"><span data-stu-id="cc60f-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-249">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="cc60f-249">System failure.</span></span> <span data-ttu-id="cc60f-250">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="cc60f-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cc60f-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cc60f-252">(24)</span><span class="sxs-lookup"><span data-stu-id="cc60f-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-253">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="cc60f-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cc60f-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cc60f-255">(25)</span><span class="sxs-lookup"><span data-stu-id="cc60f-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-256">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cc60f-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cc60f-258">(26)</span><span class="sxs-lookup"><span data-stu-id="cc60f-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-259">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cc60f-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cc60f-261">(27)</span><span class="sxs-lookup"><span data-stu-id="cc60f-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-262">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="cc60f-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cc60f-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cc60f-264">(28)</span><span class="sxs-lookup"><span data-stu-id="cc60f-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-265">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="cc60f-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cc60f-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cc60f-267">(29)</span><span class="sxs-lookup"><span data-stu-id="cc60f-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-268">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="cc60f-268">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cc60f-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cc60f-270">(30)</span><span class="sxs-lookup"><span data-stu-id="cc60f-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-271">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="cc60f-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cc60f-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc60f-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cc60f-273">(31)</span><span class="sxs-lookup"><span data-stu-id="cc60f-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-274">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="cc60f-274">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cc60f-275">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cc60f-275">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-276">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cc60f-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-278">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cc60f-278">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-279">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cc60f-279">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cc60f-280">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-280">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-281">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cc60f-281">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-282">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-284">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc60f-284">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-285">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="cc60f-285">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cc60f-286">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="cc60f-286">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cc60f-287">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-288">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc60f-288">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-291">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="cc60f-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-292">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc60f-292">Textual description of the object.</span></span>

<span data-ttu-id="cc60f-293">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-293">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-294">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cc60f-294">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-297">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc60f-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-298">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc60f-298">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="cc60f-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-300">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cc60f-300">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-301">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cc60f-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-303">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="cc60f-303">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="cc60f-304">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-305">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cc60f-305">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-306">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-308">Cadeia de caracteres de forma livre que fornece mais informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="cc60f-308">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="cc60f-309">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cc60f-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-311">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cc60f-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-313">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="cc60f-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-314">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-314">Date and time the object was installed.</span></span> <span data-ttu-id="cc60f-315">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-315">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cc60f-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cc60f-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-318">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc60f-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-320">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc60f-320">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cc60f-321">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-322">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cc60f-322">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-325">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cc60f-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-326">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="cc60f-326">Label by which the object is known.</span></span> <span data-ttu-id="cc60f-327">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="cc60f-327">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cc60f-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-329">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cc60f-329">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-332">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cc60f-332">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-333">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc60f-333">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="cc60f-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cc60f-335">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="cc60f-335">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-336">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cc60f-336">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-337">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc60f-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-339">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc60f-339">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="cc60f-340">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="cc60f-340">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc60f-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="cc60f-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cc60f-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="cc60f-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-343">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cc60f-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="cc60f-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cc60f-345"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cc60f-345"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-346">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cc60f-346">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cc60f-347"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="cc60f-347"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-348">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="cc60f-348">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cc60f-349"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="cc60f-349"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-350">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="cc60f-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="cc60f-351">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-351">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="cc60f-352">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="cc60f-352">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cc60f-353"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="cc60f-353"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-354">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="cc60f-354">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cc60f-355"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="cc60f-355"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cc60f-356">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="cc60f-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cc60f-357">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cc60f-357">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-358">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cc60f-358">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-360">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="cc60f-360">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="cc60f-361">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cc60f-361">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cc60f-362">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="cc60f-362">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="cc60f-363">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cc60f-363">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="cc60f-364">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-365">**Status**</span><span class="sxs-lookup"><span data-stu-id="cc60f-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-366">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-368">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cc60f-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-369">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cc60f-369">Current status of the object.</span></span> <span data-ttu-id="cc60f-370">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cc60f-371">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc60f-371">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cc60f-372">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cc60f-372">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cc60f-373">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="cc60f-373">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cc60f-374">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="cc60f-374">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc60f-375">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="cc60f-375">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cc60f-376">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="cc60f-376">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cc60f-377">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="cc60f-377">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cc60f-378">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="cc60f-378">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cc60f-379">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="cc60f-379">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cc60f-380">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="cc60f-380">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cc60f-381">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="cc60f-381">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cc60f-382">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="cc60f-382">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cc60f-383">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="cc60f-383">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cc60f-384">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cc60f-384">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-385">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc60f-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-386">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-387">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="cc60f-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-388">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc60f-388">State of the logical device.</span></span> <span data-ttu-id="cc60f-389">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="cc60f-389">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="cc60f-390">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cc60f-391">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cc60f-391">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc60f-392">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="cc60f-392">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cc60f-393">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cc60f-393">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cc60f-394">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="cc60f-394">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cc60f-395">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="cc60f-395">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cc60f-396">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cc60f-396">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-399">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc60f-399">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-400">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-400">Scoping system's creation class name.</span></span>

<span data-ttu-id="cc60f-401">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc60f-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cc60f-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc60f-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cc60f-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc60f-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc60f-405">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc60f-405">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc60f-406">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="cc60f-406">Scoping system's name.</span></span>

<span data-ttu-id="cc60f-407">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc60f-408">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc60f-408">Remarks</span></span>

<span data-ttu-id="cc60f-409">A classe **CIM \_ HeatPipe** é derivada de [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-409">The **CIM\_HeatPipe** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="cc60f-410">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="cc60f-410">WMI does not implement this class.</span></span> <span data-ttu-id="cc60f-411">Para classes derivadas do **CIM \_ HeatPipe**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cc60f-411">For classes derived from **CIM\_HeatPipe**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cc60f-412">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cc60f-412">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cc60f-413">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cc60f-413">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc60f-414">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc60f-414">Requirements</span></span>



| <span data-ttu-id="cc60f-415">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc60f-415">Requirement</span></span> | <span data-ttu-id="cc60f-416">Valor</span><span class="sxs-lookup"><span data-stu-id="cc60f-416">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc60f-417">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc60f-417">Minimum supported client</span></span><br/> | <span data-ttu-id="cc60f-418">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc60f-418">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc60f-419">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc60f-419">Minimum supported server</span></span><br/> | <span data-ttu-id="cc60f-420">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc60f-420">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc60f-421">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc60f-421">Namespace</span></span><br/>                | <span data-ttu-id="cc60f-422">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cc60f-422">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc60f-423">MOF</span><span class="sxs-lookup"><span data-stu-id="cc60f-423">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc60f-424"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc60f-424"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc60f-425">DLL</span><span class="sxs-lookup"><span data-stu-id="cc60f-425">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc60f-426"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc60f-426"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc60f-427">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc60f-427">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc60f-428">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="cc60f-428">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

