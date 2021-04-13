---
description: A \_ Associação de PARALLELCONTROLLER CIM está relacionada aos recursos e ao gerenciamento do dispositivo lógico de porta paralela.
ms.assetid: c05e79b6-f3a6-48cc-a831-b67e216f43eb
ms.tgt_platform: multiple
title: Classe CIM_ParallelController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParallelController
- CIM_ParallelController.Availability
- CIM_ParallelController.Capabilities
- CIM_ParallelController.CapabilityDescriptions
- CIM_ParallelController.Caption
- CIM_ParallelController.ConfigManagerErrorCode
- CIM_ParallelController.ConfigManagerUserConfig
- CIM_ParallelController.CreationClassName
- CIM_ParallelController.Description
- CIM_ParallelController.DeviceID
- CIM_ParallelController.DMASupport
- CIM_ParallelController.ErrorCleared
- CIM_ParallelController.ErrorDescription
- CIM_ParallelController.InstallDate
- CIM_ParallelController.LastErrorCode
- CIM_ParallelController.MaxNumberControlled
- CIM_ParallelController.Name
- CIM_ParallelController.PNPDeviceID
- CIM_ParallelController.PowerManagementCapabilities
- CIM_ParallelController.PowerManagementSupported
- CIM_ParallelController.ProtocolSupported
- CIM_ParallelController.Status
- CIM_ParallelController.StatusInfo
- CIM_ParallelController.SystemCreationClassName
- CIM_ParallelController.SystemName
- CIM_ParallelController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc21290de08b6e22c0bc69ec127f3c996ee5b65e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501043"
---
# <a name="cim_parallelcontroller-class"></a><span data-ttu-id="01d08-103">\_Classe CIM ParallelController</span><span class="sxs-lookup"><span data-stu-id="01d08-103">CIM\_ParallelController class</span></span>

<span data-ttu-id="01d08-104">A associação de **\_ ParallelController CIM** está relacionada aos recursos e ao gerenciamento do dispositivo lógico de porta paralela.</span><span class="sxs-lookup"><span data-stu-id="01d08-104">The **CIM\_ParallelController** association relates to the capabilities and management of the parallel port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01d08-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="01d08-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01d08-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01d08-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01d08-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="01d08-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="01d08-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="01d08-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d08-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01d08-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C552-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ParallelController : CIM_Controller
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="01d08-110">Membros</span><span class="sxs-lookup"><span data-stu-id="01d08-110">Members</span></span>

<span data-ttu-id="01d08-111">A classe **CIM \_ ParallelController** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01d08-111">The **CIM\_ParallelController** class has these types of members:</span></span>

-   [<span data-ttu-id="01d08-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="01d08-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="01d08-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01d08-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01d08-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="01d08-114">Methods</span></span>

<span data-ttu-id="01d08-115">A classe **CIM \_ ParallelController** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="01d08-115">The **CIM\_ParallelController** class has these methods.</span></span>



| <span data-ttu-id="01d08-116">Método</span><span class="sxs-lookup"><span data-stu-id="01d08-116">Method</span></span>                                                                        | <span data-ttu-id="01d08-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="01d08-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01d08-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="01d08-118">**Reset**</span></span>](reset-method-in-class-cim-parallelcontroller.md)                 | <span data-ttu-id="01d08-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="01d08-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="01d08-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="01d08-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="01d08-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="01d08-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-parallelcontroller.md) | <span data-ttu-id="01d08-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="01d08-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="01d08-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="01d08-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="01d08-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01d08-124">Properties</span></span>

<span data-ttu-id="01d08-125">A classe **CIM \_ ParallelController** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01d08-125">The **CIM\_ParallelController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01d08-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="01d08-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d08-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="01d08-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-130">Availability and status of the device.</span></span>

<span data-ttu-id="01d08-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01d08-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01d08-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01d08-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="01d08-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="01d08-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="01d08-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="01d08-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="01d08-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="01d08-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="01d08-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="01d08-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="01d08-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="01d08-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="01d08-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="01d08-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="01d08-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="01d08-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="01d08-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="01d08-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="01d08-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="01d08-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="01d08-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="01d08-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="01d08-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="01d08-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="01d08-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="01d08-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="01d08-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="01d08-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="01d08-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="01d08-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="01d08-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="01d08-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="01d08-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="01d08-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="01d08-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="01d08-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="01d08-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="01d08-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="01d08-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="01d08-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="01d08-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="01d08-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="01d08-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="01d08-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="01d08-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="01d08-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="01d08-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="01d08-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="01d08-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-161">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="01d08-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-162">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d08-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="01d08-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-164">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|As portas paralelas DMTF \| 3,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="01d08-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-165">Recursos do controlador paralelo.</span><span class="sxs-lookup"><span data-stu-id="01d08-165">Capabilities of the parallel controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01d08-166">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="01d08-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01d08-167">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01d08-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="01d08-168">**XT/at compatível** (2)</span><span class="sxs-lookup"><span data-stu-id="01d08-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="01d08-169">**Compatível com PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="01d08-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="01d08-170">**Ecp** (4)</span><span class="sxs-lookup"><span data-stu-id="01d08-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="01d08-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="01d08-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="01d08-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="01d08-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="01d08-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="01d08-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="01d08-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="01d08-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="01d08-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-176">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="01d08-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-178">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM ParallelController**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="01d08-178">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-179">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para os recursos do controlador paralelo indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="01d08-179">Free-form strings that provide detailed explanations for the parallel controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="01d08-180">Cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** , que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="01d08-180">Each entry of this array is related to the entry in the **Capabilities** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="01d08-181">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="01d08-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-184">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="01d08-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-185">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="01d08-185">Short textual description of the object.</span></span>

<span data-ttu-id="01d08-186">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="01d08-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-188">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01d08-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-189">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-190">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="01d08-190">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-191">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="01d08-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="01d08-192">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="01d08-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="01d08-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="01d08-194"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="01d08-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-195">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="01d08-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="01d08-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="01d08-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="01d08-197">(1)</span><span class="sxs-lookup"><span data-stu-id="01d08-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-198">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="01d08-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="01d08-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="01d08-200">(2)</span><span class="sxs-lookup"><span data-stu-id="01d08-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="01d08-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="01d08-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="01d08-202">(3)</span><span class="sxs-lookup"><span data-stu-id="01d08-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-203">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="01d08-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="01d08-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="01d08-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="01d08-205">(4)</span><span class="sxs-lookup"><span data-stu-id="01d08-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-206">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="01d08-206">Device is not working properly.</span></span> <span data-ttu-id="01d08-207">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="01d08-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="01d08-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="01d08-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="01d08-209">(5)</span><span class="sxs-lookup"><span data-stu-id="01d08-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-210">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="01d08-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="01d08-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="01d08-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="01d08-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="01d08-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-213">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="01d08-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="01d08-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="01d08-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="01d08-215">(7)</span><span class="sxs-lookup"><span data-stu-id="01d08-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="01d08-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="01d08-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="01d08-217">(8)</span><span class="sxs-lookup"><span data-stu-id="01d08-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-218">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="01d08-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="01d08-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="01d08-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="01d08-220">(9)</span><span class="sxs-lookup"><span data-stu-id="01d08-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-221">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-221">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="01d08-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="01d08-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="01d08-223">(10)</span><span class="sxs-lookup"><span data-stu-id="01d08-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-224">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="01d08-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="01d08-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="01d08-226">(11)</span><span class="sxs-lookup"><span data-stu-id="01d08-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-227">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="01d08-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="01d08-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="01d08-229">12</span><span class="sxs-lookup"><span data-stu-id="01d08-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-230">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="01d08-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="01d08-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="01d08-232">(13)</span><span class="sxs-lookup"><span data-stu-id="01d08-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-233">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="01d08-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="01d08-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="01d08-235">(14)</span><span class="sxs-lookup"><span data-stu-id="01d08-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-236">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="01d08-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="01d08-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="01d08-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="01d08-238">(15)</span><span class="sxs-lookup"><span data-stu-id="01d08-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-239">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="01d08-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="01d08-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="01d08-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="01d08-241">(16)</span><span class="sxs-lookup"><span data-stu-id="01d08-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-242">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="01d08-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="01d08-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="01d08-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="01d08-244">(17)</span><span class="sxs-lookup"><span data-stu-id="01d08-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-245">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="01d08-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="01d08-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="01d08-247">(18)</span><span class="sxs-lookup"><span data-stu-id="01d08-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-248">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="01d08-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="01d08-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="01d08-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="01d08-250">(19)</span><span class="sxs-lookup"><span data-stu-id="01d08-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="01d08-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="01d08-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="01d08-252">(20)</span><span class="sxs-lookup"><span data-stu-id="01d08-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-253">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="01d08-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="01d08-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="01d08-255">(21)</span><span class="sxs-lookup"><span data-stu-id="01d08-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-256">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="01d08-256">System failure.</span></span> <span data-ttu-id="01d08-257">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="01d08-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="01d08-258">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="01d08-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="01d08-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="01d08-260">(22)</span><span class="sxs-lookup"><span data-stu-id="01d08-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-261">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="01d08-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="01d08-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="01d08-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="01d08-263">(23)</span><span class="sxs-lookup"><span data-stu-id="01d08-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-264">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="01d08-264">System failure.</span></span> <span data-ttu-id="01d08-265">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="01d08-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="01d08-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="01d08-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="01d08-267">(24)</span><span class="sxs-lookup"><span data-stu-id="01d08-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-268">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="01d08-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="01d08-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="01d08-270">(25)</span><span class="sxs-lookup"><span data-stu-id="01d08-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-271">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="01d08-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="01d08-273">(26)</span><span class="sxs-lookup"><span data-stu-id="01d08-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-274">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01d08-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="01d08-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="01d08-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="01d08-276">(27)</span><span class="sxs-lookup"><span data-stu-id="01d08-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-277">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="01d08-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="01d08-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="01d08-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="01d08-279">(28)</span><span class="sxs-lookup"><span data-stu-id="01d08-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-280">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="01d08-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="01d08-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="01d08-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="01d08-282">(29)</span><span class="sxs-lookup"><span data-stu-id="01d08-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-283">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="01d08-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="01d08-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="01d08-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="01d08-285">(30)</span><span class="sxs-lookup"><span data-stu-id="01d08-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-286">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="01d08-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="01d08-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="01d08-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="01d08-288">(31)</span><span class="sxs-lookup"><span data-stu-id="01d08-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-289">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="01d08-289">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="01d08-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-291">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01d08-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-293">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="01d08-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-294">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="01d08-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="01d08-295">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="01d08-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-299">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01d08-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01d08-300">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="01d08-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="01d08-301">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="01d08-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="01d08-302">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-303">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="01d08-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-306">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="01d08-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-307">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="01d08-307">Textual description of the object.</span></span>

<span data-ttu-id="01d08-308">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="01d08-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-312">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01d08-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01d08-313">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="01d08-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="01d08-314">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-315">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="01d08-315">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-316">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01d08-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-318">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Portas paralelas DMTF \| 3,7 ")</span><span class="sxs-lookup"><span data-stu-id="01d08-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-319">Se for **true**, o acesso direto à memória (DMA) terá suporte.</span><span class="sxs-lookup"><span data-stu-id="01d08-319">If **TRUE**, direct memory access (DMA) is supported.</span></span>

</dd> <dt>

<span data-ttu-id="01d08-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="01d08-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-321">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01d08-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d08-323">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="01d08-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="01d08-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="01d08-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-326">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d08-328">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="01d08-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="01d08-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="01d08-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-331">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="01d08-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="01d08-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-334">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="01d08-334">Date and time the object was installed.</span></span> <span data-ttu-id="01d08-335">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="01d08-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="01d08-336">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="01d08-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-338">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01d08-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d08-340">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="01d08-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="01d08-341">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-342">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="01d08-342">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-343">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01d08-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-345">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="01d08-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-346">Número máximo de entidades diretamente endereçáveis com suporte pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="01d08-346">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="01d08-347">Um valor de 0 (zero) deve ser usado se o número for desconhecido ou ilimitado.</span><span class="sxs-lookup"><span data-stu-id="01d08-347">A value of 0 (zero) should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="01d08-348">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-348">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-349">**Nome**</span><span class="sxs-lookup"><span data-stu-id="01d08-349">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-352">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="01d08-352">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-353">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="01d08-353">Label by which the object is known.</span></span> <span data-ttu-id="01d08-354">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="01d08-354">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="01d08-355">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-355">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-356">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="01d08-356">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-357">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-359">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="01d08-359">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-360">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="01d08-360">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="01d08-361">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="01d08-362">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="01d08-362">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="01d08-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="01d08-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-364">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d08-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="01d08-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d08-366">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="01d08-366">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="01d08-367">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="01d08-367">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01d08-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="01d08-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="01d08-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="01d08-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="01d08-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="01d08-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="01d08-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="01d08-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-372">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="01d08-372">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="01d08-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="01d08-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-374">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="01d08-374">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="01d08-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="01d08-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-376">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="01d08-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="01d08-377">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="01d08-377">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="01d08-378">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="01d08-378">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="01d08-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="01d08-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-380">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="01d08-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="01d08-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="01d08-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="01d08-382">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="01d08-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-383">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="01d08-383">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-384">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01d08-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d08-386">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="01d08-386">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="01d08-387">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="01d08-387">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="01d08-388">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="01d08-388">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="01d08-389">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="01d08-389">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="01d08-390">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-391">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="01d08-391">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-392">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d08-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="01d08-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-395">Protocolo usado pelo controlador para acessar dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="01d08-395">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="01d08-396">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-396">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="01d08-397">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="01d08-397">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01d08-398">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01d08-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01d08-399">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="01d08-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="01d08-400">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="01d08-400">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="01d08-401">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="01d08-401">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="01d08-402">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="01d08-402">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="01d08-403">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="01d08-403">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="01d08-404">**Disquete flexível** (7)</span><span class="sxs-lookup"><span data-stu-id="01d08-404">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="01d08-405">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="01d08-405">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="01d08-406">**Interface paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="01d08-406">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="01d08-407">**Protocolo SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="01d08-407">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="01d08-408">**Protocolo de barramento serial SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="01d08-408">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="01d08-409">**Protocolo de barramento serial SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="01d08-409">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="01d08-410">**Arquitetura de armazenamento Serial SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="01d08-410">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="01d08-411">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="01d08-411">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="01d08-412">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="01d08-412">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="01d08-413">**Barramento serial universal** (16)</span><span class="sxs-lookup"><span data-stu-id="01d08-413">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="01d08-414">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="01d08-414">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="01d08-415">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="01d08-415">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="01d08-416">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="01d08-416">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="01d08-417">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="01d08-417">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="01d08-418">**Energia** (21)</span><span class="sxs-lookup"><span data-stu-id="01d08-418">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="01d08-419">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="01d08-419">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="01d08-420">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="01d08-420">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="01d08-421">**VM** (24)</span><span class="sxs-lookup"><span data-stu-id="01d08-421">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="01d08-422">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="01d08-422">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="01d08-423">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="01d08-423">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="01d08-424">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="01d08-424">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="01d08-425">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="01d08-425">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="01d08-426">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="01d08-426">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="01d08-427">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="01d08-427">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="01d08-428">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="01d08-428">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="01d08-429">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="01d08-429">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="01d08-430">**Token ring do IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="01d08-430">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="01d08-431">**ANSI X3T 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="01d08-431">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="01d08-432">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="01d08-432">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="01d08-433">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="01d08-433">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="01d08-434">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="01d08-434">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="01d08-435">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="01d08-435">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="01d08-436">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="01d08-436">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="01d08-437">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="01d08-437">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="01d08-438">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="01d08-438">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="01d08-439">**ATA/IDE avançado** (42)</span><span class="sxs-lookup"><span data-stu-id="01d08-439">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="01d08-440">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="01d08-440">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="01d08-441">**TWIRP (infravermelho bidirecional)** (44)</span><span class="sxs-lookup"><span data-stu-id="01d08-441">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="01d08-442">**Fir (infravermelho rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="01d08-442">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="01d08-443">**Sir (infravermelho serial)** (46)</span><span class="sxs-lookup"><span data-stu-id="01d08-443">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="01d08-444">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="01d08-444">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-445">**Status**</span><span class="sxs-lookup"><span data-stu-id="01d08-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-446">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-448">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="01d08-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-449">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="01d08-449">Current status of the object.</span></span> <span data-ttu-id="01d08-450">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="01d08-451">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="01d08-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="01d08-452">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="01d08-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="01d08-453">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="01d08-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="01d08-454">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="01d08-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01d08-455">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="01d08-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="01d08-456">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="01d08-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="01d08-457">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="01d08-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="01d08-458">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="01d08-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="01d08-459">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="01d08-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="01d08-460">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="01d08-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="01d08-461">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="01d08-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="01d08-462">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="01d08-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="01d08-463">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="01d08-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="01d08-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-465">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d08-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-466">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-467">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="01d08-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="01d08-468">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="01d08-468">State of the logical device.</span></span> <span data-ttu-id="01d08-469">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="01d08-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="01d08-470">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01d08-471">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01d08-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01d08-472">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="01d08-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="01d08-473">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="01d08-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="01d08-474">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="01d08-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="01d08-475">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="01d08-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d08-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="01d08-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-477">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-478">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-479">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01d08-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01d08-480">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="01d08-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="01d08-481">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="01d08-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-483">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01d08-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d08-485">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01d08-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01d08-486">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="01d08-486">Scoping system's name.</span></span>

<span data-ttu-id="01d08-487">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="01d08-488">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="01d08-488">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d08-489">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="01d08-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01d08-490">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01d08-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d08-491">Data e hora da última redefinição do controlador, o que significa que o controlador foi desligado ou reinicializado.</span><span class="sxs-lookup"><span data-stu-id="01d08-491">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="01d08-492">Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-492">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01d08-493">Comentários</span><span class="sxs-lookup"><span data-stu-id="01d08-493">Remarks</span></span>

<span data-ttu-id="01d08-494">A classe **CIM \_ ParallelController** é derivada do [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-494">The **CIM\_ParallelController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="01d08-495">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="01d08-495">WMI does not implement this class.</span></span> <span data-ttu-id="01d08-496">Para classes WMI que são derivadas do **CIM \_ ParallelController**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="01d08-496">For WMI classes that are derived from **CIM\_ParallelController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="01d08-497">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="01d08-497">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01d08-498">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="01d08-498">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d08-499">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d08-499">Requirements</span></span>



| <span data-ttu-id="01d08-500">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d08-500">Requirement</span></span> | <span data-ttu-id="01d08-501">Valor</span><span class="sxs-lookup"><span data-stu-id="01d08-501">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01d08-502">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01d08-502">Minimum supported client</span></span><br/> | <span data-ttu-id="01d08-503">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01d08-503">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01d08-504">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01d08-504">Minimum supported server</span></span><br/> | <span data-ttu-id="01d08-505">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01d08-505">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01d08-506">Namespace</span><span class="sxs-lookup"><span data-stu-id="01d08-506">Namespace</span></span><br/>                | <span data-ttu-id="01d08-507">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01d08-507">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01d08-508">MOF</span><span class="sxs-lookup"><span data-stu-id="01d08-508">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01d08-509"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01d08-509"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01d08-510">DLL</span><span class="sxs-lookup"><span data-stu-id="01d08-510">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d08-511"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d08-511"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01d08-512">Confira também</span><span class="sxs-lookup"><span data-stu-id="01d08-512">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d08-513">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="01d08-513">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

