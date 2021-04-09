---
description: A \_ classe CIM adaptador é uma classe abstrata que define os conceitos gerais de hardware de rede (por exemplo, endereço permanente ou velocidade de operação). As informações são transmitidas usando a \_ associação CIM DeviceSAPImplementation.
ms.assetid: dd44e05a-1124-42c2-aa69-340c06da35a2
ms.tgt_platform: multiple
title: Classe CIM_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter
- CIM_NetworkAdapter.AutoSense
- CIM_NetworkAdapter.Availability
- CIM_NetworkAdapter.Caption
- CIM_NetworkAdapter.ConfigManagerErrorCode
- CIM_NetworkAdapter.ConfigManagerUserConfig
- CIM_NetworkAdapter.CreationClassName
- CIM_NetworkAdapter.Description
- CIM_NetworkAdapter.DeviceID
- CIM_NetworkAdapter.ErrorCleared
- CIM_NetworkAdapter.ErrorDescription
- CIM_NetworkAdapter.InstallDate
- CIM_NetworkAdapter.LastErrorCode
- CIM_NetworkAdapter.MaxSpeed
- CIM_NetworkAdapter.Name
- CIM_NetworkAdapter.NetworkAddresses
- CIM_NetworkAdapter.PermanentAddress
- CIM_NetworkAdapter.PNPDeviceID
- CIM_NetworkAdapter.PowerManagementCapabilities
- CIM_NetworkAdapter.PowerManagementSupported
- CIM_NetworkAdapter.Speed
- CIM_NetworkAdapter.Status
- CIM_NetworkAdapter.StatusInfo
- CIM_NetworkAdapter.SystemCreationClassName
- CIM_NetworkAdapter.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76ec70bb74d74514dfe037c9e67604b29aee541a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089333"
---
# <a name="cim_networkadapter-class"></a><span data-ttu-id="da66a-104">\_Classe CIM adaptador</span><span class="sxs-lookup"><span data-stu-id="da66a-104">CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="da66a-105">A classe **CIM \_ adaptador** é uma classe abstrata que define os conceitos gerais de hardware de rede (por exemplo, endereço permanente ou velocidade de operação).</span><span class="sxs-lookup"><span data-stu-id="da66a-105">The **CIM\_NetworkAdapter** class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="da66a-106">As informações são transmitidas usando a associação [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="da66a-106">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

<span data-ttu-id="da66a-107">Os adaptadores de rede e os pontos de extremidade relacionados representam o potencial de conectividade entre os pares.</span><span class="sxs-lookup"><span data-stu-id="da66a-107">Network adapters and related endpoints represent the potential for connectivity among peers.</span></span> <span data-ttu-id="da66a-108">O potencial de conectividade é significativamente diferente do mestre ou subordinado e controlador ou de relações controladas pelo [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-108">The potential for connectivity is significantly different from the master or subordinate and controller or controlled-by relationships of [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="da66a-109">Ocasionalmente, no entanto, um único dispositivo atua como um adaptador de rede e um controlador, por exemplo, quando um adaptador de Fiber Channel opera como um controlador SCSI do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="da66a-109">Occasionally, however, a single device acts as both a network adapter and a controller, for example, when a fiber channel adapter operates as a computer system's SCSI controller.</span></span> <span data-ttu-id="da66a-110">Nesse caso, os aspectos do dispositivo são orientados por rede e outros são orientados a controlador.</span><span class="sxs-lookup"><span data-stu-id="da66a-110">In which case, aspects of the device are network oriented and others are controller oriented.</span></span> <span data-ttu-id="da66a-111">As classes de controlador e adaptador devem ser instanciadas e uma relação de identidade de dispositivo também deve ser criada para vincular os diferentes aspectos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-111">The controller and adapter classes should be instantiated and a device identity relationship should also be created to link the different aspects of the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da66a-112">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="da66a-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da66a-113">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="da66a-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da66a-114">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="da66a-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="da66a-115">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="da66a-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="da66a-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da66a-116">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C532-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_NetworkAdapter : CIM_LogicalDevice
{
  boolean  AutoSense;
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
  uint64   MaxSpeed;
  string   Name;
  string   NetworkAddresses[];
  string   PermanentAddress;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="da66a-117">Membros</span><span class="sxs-lookup"><span data-stu-id="da66a-117">Members</span></span>

<span data-ttu-id="da66a-118">A classe **CIM \_ adaptador** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="da66a-118">The **CIM\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="da66a-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="da66a-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="da66a-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da66a-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da66a-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="da66a-121">Methods</span></span>

<span data-ttu-id="da66a-122">A classe **CIM \_ adaptador** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="da66a-122">The **CIM\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="da66a-123">Método</span><span class="sxs-lookup"><span data-stu-id="da66a-123">Method</span></span>                                                                    | <span data-ttu-id="da66a-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="da66a-124">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da66a-125">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="da66a-125">**Reset**</span></span>](reset-method-in-class-cim-networkadapter.md)                 | <span data-ttu-id="da66a-126">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="da66a-126">Requests a reset of the logical device.</span></span> <span data-ttu-id="da66a-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="da66a-127">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="da66a-128">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="da66a-128">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-networkadapter.md) | <span data-ttu-id="da66a-129">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="da66a-129">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="da66a-130">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="da66a-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="da66a-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="da66a-131">Properties</span></span>

<span data-ttu-id="da66a-132">A classe **CIM \_ adaptador** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="da66a-132">The **CIM\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da66a-133">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="da66a-133">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-134">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da66a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da66a-136">Se **for true**, o adaptador de rede poderá determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada.</span><span class="sxs-lookup"><span data-stu-id="da66a-136">If **TRUE**, the network adapter can automatically determine the speed or other communications characteristics of the attached network media.</span></span>

</dd> <dt>

<span data-ttu-id="da66a-137">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="da66a-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-138">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da66a-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="da66a-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-141">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-141">Availability and status of the device.</span></span>

<span data-ttu-id="da66a-142">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="da66a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="da66a-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da66a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="da66a-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="da66a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="da66a-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="da66a-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="da66a-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="da66a-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="da66a-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="da66a-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="da66a-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="da66a-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="da66a-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="da66a-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="da66a-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="da66a-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="da66a-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="da66a-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="da66a-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="da66a-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="da66a-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="da66a-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="da66a-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="da66a-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="da66a-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-156">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="da66a-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="da66a-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="da66a-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-158">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="da66a-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="da66a-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="da66a-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-160">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="da66a-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="da66a-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="da66a-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="da66a-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="da66a-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-163">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="da66a-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="da66a-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="da66a-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-165">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="da66a-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="da66a-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="da66a-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-167">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="da66a-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="da66a-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="da66a-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-169">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="da66a-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="da66a-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="da66a-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-171">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="da66a-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="da66a-172">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="da66a-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-175">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="da66a-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-176">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="da66a-176">Short textual description of the object.</span></span>

<span data-ttu-id="da66a-177">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="da66a-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-179">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da66a-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-181">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="da66a-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-182">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="da66a-182">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="da66a-183">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="da66a-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="da66a-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="da66a-185"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="da66a-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-186">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="da66a-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="da66a-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="da66a-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="da66a-188">(1)</span><span class="sxs-lookup"><span data-stu-id="da66a-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-189">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="da66a-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="da66a-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="da66a-191">(2)</span><span class="sxs-lookup"><span data-stu-id="da66a-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="da66a-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="da66a-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="da66a-193">(3)</span><span class="sxs-lookup"><span data-stu-id="da66a-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-194">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="da66a-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="da66a-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="da66a-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="da66a-196">(4)</span><span class="sxs-lookup"><span data-stu-id="da66a-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-197">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="da66a-197">Device is not working properly.</span></span> <span data-ttu-id="da66a-198">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="da66a-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="da66a-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="da66a-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="da66a-200">(5)</span><span class="sxs-lookup"><span data-stu-id="da66a-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-201">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="da66a-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="da66a-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="da66a-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="da66a-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="da66a-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-204">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="da66a-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="da66a-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="da66a-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="da66a-206">(7)</span><span class="sxs-lookup"><span data-stu-id="da66a-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="da66a-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="da66a-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="da66a-208">(8)</span><span class="sxs-lookup"><span data-stu-id="da66a-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-209">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="da66a-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="da66a-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="da66a-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="da66a-211">(9)</span><span class="sxs-lookup"><span data-stu-id="da66a-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-212">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="da66a-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="da66a-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="da66a-214">(10)</span><span class="sxs-lookup"><span data-stu-id="da66a-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-215">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="da66a-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="da66a-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="da66a-217">(11)</span><span class="sxs-lookup"><span data-stu-id="da66a-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-218">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="da66a-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="da66a-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="da66a-220">12</span><span class="sxs-lookup"><span data-stu-id="da66a-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-221">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="da66a-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="da66a-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="da66a-223">(13)</span><span class="sxs-lookup"><span data-stu-id="da66a-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-224">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="da66a-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="da66a-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="da66a-226">(14)</span><span class="sxs-lookup"><span data-stu-id="da66a-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-227">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="da66a-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="da66a-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="da66a-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="da66a-229">(15)</span><span class="sxs-lookup"><span data-stu-id="da66a-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-230">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="da66a-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="da66a-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="da66a-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="da66a-232">(16)</span><span class="sxs-lookup"><span data-stu-id="da66a-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-233">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="da66a-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="da66a-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="da66a-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="da66a-235">(17)</span><span class="sxs-lookup"><span data-stu-id="da66a-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-236">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="da66a-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="da66a-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="da66a-238">(18)</span><span class="sxs-lookup"><span data-stu-id="da66a-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-239">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="da66a-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="da66a-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="da66a-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="da66a-241">(19)</span><span class="sxs-lookup"><span data-stu-id="da66a-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="da66a-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="da66a-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="da66a-243">(20)</span><span class="sxs-lookup"><span data-stu-id="da66a-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-244">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="da66a-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="da66a-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="da66a-246">(21)</span><span class="sxs-lookup"><span data-stu-id="da66a-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-247">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="da66a-247">System failure.</span></span> <span data-ttu-id="da66a-248">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="da66a-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="da66a-249">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="da66a-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="da66a-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="da66a-251">(22)</span><span class="sxs-lookup"><span data-stu-id="da66a-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-252">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="da66a-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="da66a-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="da66a-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="da66a-254">(23)</span><span class="sxs-lookup"><span data-stu-id="da66a-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-255">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="da66a-255">System failure.</span></span> <span data-ttu-id="da66a-256">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="da66a-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="da66a-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="da66a-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="da66a-258">(24)</span><span class="sxs-lookup"><span data-stu-id="da66a-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-259">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="da66a-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="da66a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="da66a-261">(25)</span><span class="sxs-lookup"><span data-stu-id="da66a-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-262">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="da66a-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="da66a-264">(26)</span><span class="sxs-lookup"><span data-stu-id="da66a-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-265">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da66a-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="da66a-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="da66a-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="da66a-267">(27)</span><span class="sxs-lookup"><span data-stu-id="da66a-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-268">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="da66a-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="da66a-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="da66a-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="da66a-270">(28)</span><span class="sxs-lookup"><span data-stu-id="da66a-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-271">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="da66a-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="da66a-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="da66a-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="da66a-273">(29)</span><span class="sxs-lookup"><span data-stu-id="da66a-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-274">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="da66a-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="da66a-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="da66a-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="da66a-276">(30)</span><span class="sxs-lookup"><span data-stu-id="da66a-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-277">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="da66a-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="da66a-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="da66a-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="da66a-279">(31)</span><span class="sxs-lookup"><span data-stu-id="da66a-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-280">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="da66a-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="da66a-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="da66a-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-282">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da66a-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-284">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="da66a-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-285">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="da66a-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="da66a-286">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="da66a-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-290">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="da66a-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="da66a-291">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="da66a-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="da66a-292">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="da66a-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="da66a-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-294">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="da66a-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-297">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="da66a-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-298">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="da66a-298">Textual description of the object.</span></span>

<span data-ttu-id="da66a-299">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-300">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="da66a-300">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-303">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="da66a-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="da66a-304">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="da66a-304">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="da66a-305">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-306">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="da66a-306">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-307">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da66a-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-308">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da66a-309">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="da66a-309">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="da66a-310">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-311">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="da66a-311">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da66a-314">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="da66a-314">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="da66a-315">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-316">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da66a-316">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-317">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da66a-317">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-319">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="da66a-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-320">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="da66a-320">Date and time the object was installed.</span></span> <span data-ttu-id="da66a-321">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="da66a-321">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="da66a-322">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-323">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="da66a-323">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-324">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da66a-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da66a-326">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="da66a-326">Last error code reported by the logical device.</span></span>

<span data-ttu-id="da66a-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-328">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="da66a-328">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-329">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da66a-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-331">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="da66a-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-332">Velocidade máxima, em bits por segundo (BPS), para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="da66a-332">Maximum speed, in bits per second (BPS), for the network adapter.</span></span>

<span data-ttu-id="da66a-333">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="da66a-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-334">**Nome**</span><span class="sxs-lookup"><span data-stu-id="da66a-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-337">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="da66a-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-338">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="da66a-338">Label by which the object is known.</span></span> <span data-ttu-id="da66a-339">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="da66a-339">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="da66a-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-341">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="da66a-341">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-342">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da66a-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-344">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de rede DMTF 802 porta \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="da66a-344">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-345">Lista de endereços de rede para um adaptador.</span><span class="sxs-lookup"><span data-stu-id="da66a-345">List of network addresses for an adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da66a-346">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="da66a-346">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-349">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de rede DMTF 802 porta \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="da66a-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-350">Endereço de rede embutido em código em um adaptador.</span><span class="sxs-lookup"><span data-stu-id="da66a-350">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="da66a-351">O endereço embutido em código pode ser alterado com uma atualização de firmware ou configuração de software.</span><span class="sxs-lookup"><span data-stu-id="da66a-351">The hard-coded address can be changed with a firmware upgrade or software configuration.</span></span> <span data-ttu-id="da66a-352">Se for alterado, o campo deverá ser atualizado quando a alteração for feita.</span><span class="sxs-lookup"><span data-stu-id="da66a-352">If changed, the field should be updated when the change is made.</span></span> <span data-ttu-id="da66a-353">Essa propriedade deve ser deixada em branco se não existir nenhum endereço embutido no código para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="da66a-353">This property should be left blank if no hard-coded address exists for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="da66a-354">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="da66a-354">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-357">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="da66a-357">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-358">O Win32 Plug and Play identificador de dispositivo do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="da66a-358">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="da66a-359">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="da66a-360">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="da66a-360">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="da66a-361">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="da66a-361">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-362">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da66a-362">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da66a-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da66a-364">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="da66a-364">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="da66a-365">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="da66a-365">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da66a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="da66a-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="da66a-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="da66a-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="da66a-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="da66a-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="da66a-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="da66a-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-370">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="da66a-370">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="da66a-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="da66a-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-372">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="da66a-372">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="da66a-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="da66a-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-374">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="da66a-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="da66a-375">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="da66a-375">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="da66a-376">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="da66a-376">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="da66a-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="da66a-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-378">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="da66a-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="da66a-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="da66a-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="da66a-380">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="da66a-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="da66a-381">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="da66a-381">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-382">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="da66a-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da66a-384">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="da66a-384">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="da66a-385">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="da66a-385">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="da66a-386">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="da66a-386">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="da66a-387">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="da66a-387">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="da66a-388">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-388">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-389">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="da66a-389">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-390">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da66a-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-392">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Adaptador de rede DMTF 802 porta \| 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits por segundo ")</span><span class="sxs-lookup"><span data-stu-id="da66a-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-393">Estimativa da largura de banda atual, em BPS.</span><span class="sxs-lookup"><span data-stu-id="da66a-393">Estimate of the current bandwidth, in BPS.</span></span> <span data-ttu-id="da66a-394">Para pontos de extremidade que variam de largura de banda ou para aqueles em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="da66a-394">For endpoints that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="da66a-395">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="da66a-395">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-396">**Status**</span><span class="sxs-lookup"><span data-stu-id="da66a-396">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-397">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-399">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="da66a-399">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-400">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="da66a-400">Current status of the object.</span></span>

<span data-ttu-id="da66a-401">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="da66a-402">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="da66a-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="da66a-403">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="da66a-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="da66a-404">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="da66a-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="da66a-405">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="da66a-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da66a-406">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="da66a-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="da66a-407">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="da66a-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="da66a-408">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="da66a-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="da66a-409">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="da66a-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="da66a-410">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="da66a-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="da66a-411">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="da66a-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="da66a-412">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="da66a-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="da66a-413">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="da66a-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="da66a-414">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="da66a-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="da66a-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="da66a-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-416">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da66a-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-417">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-418">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="da66a-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="da66a-419">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="da66a-419">State of the logical device.</span></span> <span data-ttu-id="da66a-420">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="da66a-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="da66a-421">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="da66a-422">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="da66a-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="da66a-423">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="da66a-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="da66a-424">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="da66a-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="da66a-425">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="da66a-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="da66a-426">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="da66a-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="da66a-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="da66a-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-430">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="da66a-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="da66a-431">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="da66a-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="da66a-432">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="da66a-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="da66a-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da66a-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="da66a-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da66a-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="da66a-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da66a-436">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="da66a-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="da66a-437">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="da66a-437">Scoping system's name.</span></span>

<span data-ttu-id="da66a-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da66a-439">Comentários</span><span class="sxs-lookup"><span data-stu-id="da66a-439">Remarks</span></span>

<span data-ttu-id="da66a-440">A classe **CIM \_ adaptador** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-440">The **CIM\_NetworkAdapter** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="da66a-441">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="da66a-441">WMI does not implement this class.</span></span> <span data-ttu-id="da66a-442">Para classes derivadas do **CIM \_ adaptador**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="da66a-442">For classes that are derived from **CIM\_NetworkAdapter**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="da66a-443">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="da66a-443">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da66a-444">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="da66a-444">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da66a-445">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da66a-445">Requirements</span></span>



| <span data-ttu-id="da66a-446">Requisito</span><span class="sxs-lookup"><span data-stu-id="da66a-446">Requirement</span></span> | <span data-ttu-id="da66a-447">Valor</span><span class="sxs-lookup"><span data-stu-id="da66a-447">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da66a-448">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da66a-448">Minimum supported client</span></span><br/> | <span data-ttu-id="da66a-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da66a-449">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da66a-450">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da66a-450">Minimum supported server</span></span><br/> | <span data-ttu-id="da66a-451">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da66a-451">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da66a-452">Namespace</span><span class="sxs-lookup"><span data-stu-id="da66a-452">Namespace</span></span><br/>                | <span data-ttu-id="da66a-453">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="da66a-453">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da66a-454">MOF</span><span class="sxs-lookup"><span data-stu-id="da66a-454">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da66a-455"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da66a-455"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da66a-456">DLL</span><span class="sxs-lookup"><span data-stu-id="da66a-456">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da66a-457"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da66a-457"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da66a-458">Confira também</span><span class="sxs-lookup"><span data-stu-id="da66a-458">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da66a-459">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="da66a-459">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

