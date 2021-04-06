---
description: A \_ classe CIM TapeDrive representa uma unidade de fita no sistema. As unidades de fita são basicamente diferenciadas, pois só podem ser acessadas sequencialmente.
ms.assetid: 8b7f2277-e37d-4597-81bb-d3c8d4966a81
ms.tgt_platform: multiple
title: Classe CIM_TapeDrive (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.Availability
- CIM_TapeDrive.Capabilities
- CIM_TapeDrive.CapabilityDescriptions
- CIM_TapeDrive.Caption
- CIM_TapeDrive.CompressionMethod
- CIM_TapeDrive.ConfigManagerErrorCode
- CIM_TapeDrive.ConfigManagerUserConfig
- CIM_TapeDrive.CreationClassName
- CIM_TapeDrive.DefaultBlockSize
- CIM_TapeDrive.Description
- CIM_TapeDrive.DeviceID
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.ErrorCleared
- CIM_TapeDrive.ErrorDescription
- CIM_TapeDrive.ErrorMethodology
- CIM_TapeDrive.InstallDate
- CIM_TapeDrive.LastErrorCode
- CIM_TapeDrive.MaxBlockSize
- CIM_TapeDrive.MaxMediaSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.MinBlockSize
- CIM_TapeDrive.Name
- CIM_TapeDrive.NeedsCleaning
- CIM_TapeDrive.NumberOfMediaSupported
- CIM_TapeDrive.Padding
- CIM_TapeDrive.PNPDeviceID
- CIM_TapeDrive.PowerManagementCapabilities
- CIM_TapeDrive.PowerManagementSupported
- CIM_TapeDrive.Status
- CIM_TapeDrive.StatusInfo
- CIM_TapeDrive.SystemCreationClassName
- CIM_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 184b855d5989c77292e51e8b477c5392893deccb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826711"
---
# <a name="cim_tapedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="22de3-104">Classe CIM_TapeDrive (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="22de3-104">CIM_TapeDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="22de3-105">A classe **CIM \_ TapeDrive** representa uma unidade de fita no sistema.</span><span class="sxs-lookup"><span data-stu-id="22de3-105">The **CIM\_TapeDrive** class represents a tape drive on the system.</span></span> <span data-ttu-id="22de3-106">As unidades de fita são basicamente diferenciadas, pois só podem ser acessadas sequencialmente.</span><span class="sxs-lookup"><span data-stu-id="22de3-106">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22de3-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="22de3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="22de3-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="22de3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="22de3-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="22de3-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="22de3-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="22de3-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="22de3-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22de3-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="22de3-112">Membros</span><span class="sxs-lookup"><span data-stu-id="22de3-112">Members</span></span>

<span data-ttu-id="22de3-113">A classe **CIM \_ TapeDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="22de3-113">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="22de3-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="22de3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="22de3-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22de3-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22de3-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="22de3-116">Methods</span></span>

<span data-ttu-id="22de3-117">A classe **CIM \_ TapeDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="22de3-117">The **CIM\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="22de3-118">Método</span><span class="sxs-lookup"><span data-stu-id="22de3-118">Method</span></span>                                                               | <span data-ttu-id="22de3-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="22de3-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22de3-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="22de3-120">**Reset**</span></span>](reset-method-in-class-cim-tapedrive.md)                 | <span data-ttu-id="22de3-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="22de3-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="22de3-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="22de3-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="22de3-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tapedrive.md) | <span data-ttu-id="22de3-124">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="22de3-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="22de3-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="22de3-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22de3-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22de3-126">Properties</span></span>

<span data-ttu-id="22de3-127">A classe **CIM \_ TapeDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="22de3-127">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22de3-128">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="22de3-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22de3-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="22de3-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-132">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-132">Availability and status of the device.</span></span>

<span data-ttu-id="22de3-133">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22de3-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22de3-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22de3-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="22de3-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="22de3-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="22de3-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="22de3-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="22de3-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="22de3-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="22de3-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="22de3-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="22de3-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="22de3-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="22de3-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="22de3-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="22de3-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="22de3-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="22de3-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="22de3-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="22de3-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="22de3-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="22de3-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="22de3-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="22de3-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="22de3-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="22de3-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-147">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="22de3-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="22de3-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="22de3-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-149">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="22de3-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="22de3-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="22de3-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-151">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="22de3-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="22de3-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="22de3-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="22de3-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-154">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="22de3-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="22de3-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="22de3-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-156">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="22de3-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="22de3-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="22de3-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-158">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="22de3-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="22de3-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="22de3-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-160">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="22de3-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="22de3-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="22de3-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-162">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="22de3-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-163">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="22de3-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-164">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22de3-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22de3-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-166">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="22de3-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-167">Recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="22de3-167">Capabilities of the media access device.</span></span> <span data-ttu-id="22de3-168">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-168">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22de3-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22de3-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-170">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="22de3-170">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22de3-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22de3-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-172">Outros.</span><span class="sxs-lookup"><span data-stu-id="22de3-172">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="22de3-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="22de3-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-174">Acesso sequencial.</span><span class="sxs-lookup"><span data-stu-id="22de3-174">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="22de3-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="22de3-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-176">Acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="22de3-176">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="22de3-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="22de3-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-178">Criando.</span><span class="sxs-lookup"><span data-stu-id="22de3-178">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="22de3-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="22de3-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-180">Criptografia.</span><span class="sxs-lookup"><span data-stu-id="22de3-180">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="22de3-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="22de3-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-182">Compactação.</span><span class="sxs-lookup"><span data-stu-id="22de3-182">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="22de3-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="22de3-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-184">Mídia removível.</span><span class="sxs-lookup"><span data-stu-id="22de3-184">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="22de3-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="22de3-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-186">Limpeza manual.</span><span class="sxs-lookup"><span data-stu-id="22de3-186">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="22de3-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="22de3-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-188">Limpeza automática.</span><span class="sxs-lookup"><span data-stu-id="22de3-188">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="22de3-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="22de3-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-190">Notificação inteligente.</span><span class="sxs-lookup"><span data-stu-id="22de3-190">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="22de3-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="22de3-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-192">Distingue um dispositivo que pode acessar ambos os lados da mídia de dois lados de um dispositivo que lê apenas um único lado e requer que a mídia seja transferida.</span><span class="sxs-lookup"><span data-stu-id="22de3-192">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="22de3-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="22de3-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-194">Indica que a mídia não precisa ser desejetada explicitamente do dispositivo antes de ser acessada por um elemento de seletor.</span><span class="sxs-lookup"><span data-stu-id="22de3-194">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-195">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22de3-195">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-196">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-196">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22de3-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-198">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="22de3-198">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-199">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para os recursos de dispositivo de acesso indicados na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="22de3-199">Free-form strings that provide detailed explanations for the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="22de3-200">Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="22de3-200">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="22de3-201">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-202">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="22de3-202">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-205">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="22de3-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-206">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="22de3-206">Short textual description of the object.</span></span>

<span data-ttu-id="22de3-207">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-207">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-208">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="22de3-208">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-209">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-211">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-211">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="22de3-212">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="22de3-212">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="22de3-213">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="22de3-213">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="22de3-214">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="22de3-214">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="22de3-215">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-215">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="22de3-216">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="22de3-216">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="22de3-217">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="22de3-217">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="22de3-218">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="22de3-218">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="22de3-219">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="22de3-219">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="22de3-220">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="22de3-220">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="22de3-221">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="22de3-221">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-222">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22de3-222">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-223">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22de3-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-225">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="22de3-225">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-226">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="22de3-226">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="22de3-227">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-227">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="22de3-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="22de3-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="22de3-229"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="22de3-229">(0)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-230">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-230">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="22de3-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="22de3-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="22de3-232">(1)</span><span class="sxs-lookup"><span data-stu-id="22de3-232">(1)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-233">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-233">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="22de3-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="22de3-235">(2)</span><span class="sxs-lookup"><span data-stu-id="22de3-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="22de3-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="22de3-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="22de3-237">(3)</span><span class="sxs-lookup"><span data-stu-id="22de3-237">(3)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-238">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="22de3-238">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="22de3-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="22de3-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="22de3-240">(4)</span><span class="sxs-lookup"><span data-stu-id="22de3-240">(4)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-241">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-241">Device is not working properly.</span></span> <span data-ttu-id="22de3-242">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="22de3-242">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="22de3-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="22de3-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="22de3-244">(5)</span><span class="sxs-lookup"><span data-stu-id="22de3-244">(5)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-245">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="22de3-245">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="22de3-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="22de3-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="22de3-247"> (6)</span><span class="sxs-lookup"><span data-stu-id="22de3-247">(6)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-248">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="22de3-248">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="22de3-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="22de3-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="22de3-250">(7)</span><span class="sxs-lookup"><span data-stu-id="22de3-250">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="22de3-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="22de3-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="22de3-252">(8)</span><span class="sxs-lookup"><span data-stu-id="22de3-252">(8)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-253">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="22de3-253">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="22de3-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="22de3-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="22de3-255">(9)</span><span class="sxs-lookup"><span data-stu-id="22de3-255">(9)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-256">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-256">Device is not working properly.</span></span> <span data-ttu-id="22de3-257">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-257">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="22de3-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="22de3-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="22de3-259">(10)</span><span class="sxs-lookup"><span data-stu-id="22de3-259">(10)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-260">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-260">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="22de3-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="22de3-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="22de3-262">(11)</span><span class="sxs-lookup"><span data-stu-id="22de3-262">(11)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-263">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-263">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="22de3-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="22de3-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="22de3-265">12</span><span class="sxs-lookup"><span data-stu-id="22de3-265">(12)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-266">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="22de3-266">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="22de3-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="22de3-268">(13)</span><span class="sxs-lookup"><span data-stu-id="22de3-268">(13)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-269">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-269">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="22de3-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="22de3-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="22de3-271">(14)</span><span class="sxs-lookup"><span data-stu-id="22de3-271">(14)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-272">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="22de3-272">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="22de3-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="22de3-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="22de3-274">(15)</span><span class="sxs-lookup"><span data-stu-id="22de3-274">(15)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-275">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="22de3-275">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="22de3-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="22de3-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="22de3-277">(16)</span><span class="sxs-lookup"><span data-stu-id="22de3-277">(16)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-278">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="22de3-278">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="22de3-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="22de3-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="22de3-280">(17)</span><span class="sxs-lookup"><span data-stu-id="22de3-280">(17)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-281">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="22de3-281">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="22de3-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="22de3-283">(18)</span><span class="sxs-lookup"><span data-stu-id="22de3-283">(18)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-284">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="22de3-284">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="22de3-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="22de3-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="22de3-286">(19)</span><span class="sxs-lookup"><span data-stu-id="22de3-286">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="22de3-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="22de3-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="22de3-288">(20)</span><span class="sxs-lookup"><span data-stu-id="22de3-288">(20)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-289">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="22de3-289">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="22de3-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="22de3-291">(21)</span><span class="sxs-lookup"><span data-stu-id="22de3-291">(21)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-292">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="22de3-292">System failure.</span></span> <span data-ttu-id="22de3-293">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="22de3-293">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="22de3-294">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-294">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="22de3-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="22de3-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="22de3-296">(22)</span><span class="sxs-lookup"><span data-stu-id="22de3-296">(22)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-297">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="22de3-297">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="22de3-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="22de3-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="22de3-299">(23)</span><span class="sxs-lookup"><span data-stu-id="22de3-299">(23)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-300">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="22de3-300">System failure.</span></span> <span data-ttu-id="22de3-301">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="22de3-301">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="22de3-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="22de3-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="22de3-303">(24)</span><span class="sxs-lookup"><span data-stu-id="22de3-303">(24)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-304">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="22de3-304">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="22de3-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="22de3-306">(25)</span><span class="sxs-lookup"><span data-stu-id="22de3-306">(25)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-307">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="22de3-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="22de3-309">(26)</span><span class="sxs-lookup"><span data-stu-id="22de3-309">(26)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-310">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-310">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="22de3-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="22de3-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="22de3-312">(27)</span><span class="sxs-lookup"><span data-stu-id="22de3-312">(27)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-313">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="22de3-313">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="22de3-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="22de3-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="22de3-315">(28)</span><span class="sxs-lookup"><span data-stu-id="22de3-315">(28)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-316">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="22de3-316">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="22de3-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="22de3-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="22de3-318">(29)</span><span class="sxs-lookup"><span data-stu-id="22de3-318">(29)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-319">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="22de3-319">Device is disabled.</span></span> <span data-ttu-id="22de3-320">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="22de3-320">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="22de3-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="22de3-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="22de3-322">(30)</span><span class="sxs-lookup"><span data-stu-id="22de3-322">(30)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-323">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="22de3-323">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="22de3-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22de3-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="22de3-325">(31)</span><span class="sxs-lookup"><span data-stu-id="22de3-325">(31)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-326">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-326">Device is not working properly.</span></span> <span data-ttu-id="22de3-327">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="22de3-327">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-328">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="22de3-328">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-329">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22de3-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-331">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="22de3-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-332">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="22de3-332">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="22de3-333">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-333">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-334">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22de3-334">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-337">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22de3-337">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22de3-338">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="22de3-338">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="22de3-339">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="22de3-339">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="22de3-340">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-341">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="22de3-341">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-342">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22de3-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-344">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22de3-344">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-345">Tamanho de bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-345">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="22de3-346">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-346">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="22de3-347">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="22de3-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-348">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="22de3-348">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-351">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="22de3-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-352">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="22de3-352">Textual description of the object.</span></span>

<span data-ttu-id="22de3-353">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-353">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-354">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="22de3-354">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-357">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22de3-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22de3-358">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-358">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="22de3-359">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-360">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="22de3-360">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-361">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22de3-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-363">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22de3-363">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-364">Tamanho, em bytes, da área designada como fim da fita.</span><span class="sxs-lookup"><span data-stu-id="22de3-364">Size, in bytes, of the area designated as end-of-tape.</span></span> <span data-ttu-id="22de3-365">O acesso nessa área gera um aviso de fim de fita.</span><span class="sxs-lookup"><span data-stu-id="22de3-365">Access in this area generates an end-of-tape warning.</span></span>

</dd> <dt>

<span data-ttu-id="22de3-366">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="22de3-366">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-367">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22de3-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-369">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="22de3-369">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="22de3-370">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-371">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="22de3-371">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-372">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-374">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="22de3-374">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="22de3-375">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-376">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="22de3-376">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-377">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-379">Cadeia de caracteres de forma livre que descreve os tipos de detecção de erro e correção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-379">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="22de3-380">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-380">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-381">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22de3-381">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-382">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22de3-382">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-384">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="22de3-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-385">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="22de3-385">Date and time the object was installed.</span></span> <span data-ttu-id="22de3-386">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="22de3-386">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="22de3-387">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-388">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22de3-388">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-389">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22de3-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-391">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-391">Last error code reported by the logical device.</span></span>

<span data-ttu-id="22de3-392">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-393">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="22de3-393">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-394">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22de3-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-396">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22de3-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-397">Tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-397">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="22de3-398">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-398">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="22de3-399">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="22de3-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-400">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="22de3-400">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-401">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22de3-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-402">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-403">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="22de3-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-404">Tamanho máximo, em quilobytes, de mídia com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-404">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="22de3-405">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="22de3-405">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="22de3-406">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-406">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="22de3-407">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="22de3-407">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-408">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="22de3-408">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-409">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22de3-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-411">Contagem máxima de partições para a unidade de fita.</span><span class="sxs-lookup"><span data-stu-id="22de3-411">Maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="22de3-412">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="22de3-412">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-413">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22de3-413">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-415">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22de3-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-416">Tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-416">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="22de3-417">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="22de3-418">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="22de3-418">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-419">**Nome**</span><span class="sxs-lookup"><span data-stu-id="22de3-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-420">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-422">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="22de3-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-423">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="22de3-423">Label by which the object is known.</span></span> <span data-ttu-id="22de3-424">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="22de3-424">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="22de3-425">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-426">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="22de3-426">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-427">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22de3-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-429">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="22de3-429">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="22de3-430">A limpeza manual ou automática é possível é indicada na propriedade da matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="22de3-430">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="22de3-431">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-432">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="22de3-432">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-433">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22de3-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-434">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-435">Quando o dispositivo de acesso à mídia dá suporte a várias mídias individuais, essa propriedade define o número máximo que pode ser suportado ou inserido.</span><span class="sxs-lookup"><span data-stu-id="22de3-435">When the media access device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

<span data-ttu-id="22de3-436">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-436">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-437">**Preenchimento**</span><span class="sxs-lookup"><span data-stu-id="22de3-437">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-438">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22de3-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-440">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22de3-440">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-441">Número de bytes inseridos entre os blocos em uma mídia de fita.</span><span class="sxs-lookup"><span data-stu-id="22de3-441">Number of bytes inserted between blocks on a tape media.</span></span>

</dd> <dt>

<span data-ttu-id="22de3-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="22de3-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-445">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="22de3-445">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-446">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-446">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="22de3-447">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="22de3-448">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="22de3-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="22de3-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="22de3-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-450">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22de3-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22de3-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-452">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="22de3-453">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="22de3-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22de3-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22de3-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="22de3-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="22de3-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-456">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22de3-456">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="22de3-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="22de3-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="22de3-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="22de3-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-459">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="22de3-459">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="22de3-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="22de3-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-461">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="22de3-461">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="22de3-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="22de3-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-463">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="22de3-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="22de3-464">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="22de3-464">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="22de3-465">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="22de3-465">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="22de3-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="22de3-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-467">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="22de3-467">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="22de3-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="22de3-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="22de3-469">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="22de3-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="22de3-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-471">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22de3-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22de3-473">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="22de3-473">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="22de3-474">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="22de3-474">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="22de3-475">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="22de3-475">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="22de3-476">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="22de3-476">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="22de3-477">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-478">**Status**</span><span class="sxs-lookup"><span data-stu-id="22de3-478">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-479">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-480">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-481">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="22de3-481">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-482">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="22de3-482">Current status of the object.</span></span> <span data-ttu-id="22de3-483">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-483">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="22de3-484">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="22de3-484">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="22de3-485">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="22de3-485">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="22de3-486">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="22de3-486">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="22de3-487">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="22de3-487">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22de3-488">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="22de3-488">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="22de3-489">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="22de3-489">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="22de3-490">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="22de3-490">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="22de3-491">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="22de3-491">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="22de3-492">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="22de3-492">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="22de3-493">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="22de3-493">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="22de3-494">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="22de3-494">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="22de3-495">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="22de3-495">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="22de3-496">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="22de3-496">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-497">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="22de3-497">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-498">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22de3-498">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-499">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-500">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="22de3-500">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="22de3-501">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22de3-501">State of the logical device.</span></span> <span data-ttu-id="22de3-502">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="22de3-502">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="22de3-503">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22de3-504">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22de3-504">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22de3-505">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="22de3-505">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="22de3-506">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="22de3-506">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="22de3-507">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="22de3-507">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="22de3-508">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="22de3-508">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22de3-509">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22de3-509">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-510">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-511">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-512">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22de3-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22de3-513">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="22de3-513">Scoping system's creation class name.</span></span>

<span data-ttu-id="22de3-514">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22de3-515">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="22de3-515">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22de3-516">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22de3-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22de3-517">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22de3-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22de3-518">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22de3-518">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22de3-519">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="22de3-519">Scoping system's name.</span></span>

<span data-ttu-id="22de3-520">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-520">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22de3-521">Comentários</span><span class="sxs-lookup"><span data-stu-id="22de3-521">Remarks</span></span>

<span data-ttu-id="22de3-522">A classe **CIM \_ TapeDrive** é derivada de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-522">The **CIM\_TapeDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="22de3-523">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="22de3-523">WMI does not implement this class.</span></span> <span data-ttu-id="22de3-524">Para classes WMI derivadas do **CIM \_ TapeDrive**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22de3-524">For WMI classes derived from **CIM\_TapeDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="22de3-525">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="22de3-525">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="22de3-526">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="22de3-526">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="22de3-527">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22de3-527">Requirements</span></span>



| <span data-ttu-id="22de3-528">Requisito</span><span class="sxs-lookup"><span data-stu-id="22de3-528">Requirement</span></span> | <span data-ttu-id="22de3-529">Valor</span><span class="sxs-lookup"><span data-stu-id="22de3-529">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22de3-530">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22de3-530">Minimum supported client</span></span><br/> | <span data-ttu-id="22de3-531">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22de3-531">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22de3-532">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22de3-532">Minimum supported server</span></span><br/> | <span data-ttu-id="22de3-533">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22de3-533">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22de3-534">Namespace</span><span class="sxs-lookup"><span data-stu-id="22de3-534">Namespace</span></span><br/>                | <span data-ttu-id="22de3-535">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="22de3-535">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22de3-536">MOF</span><span class="sxs-lookup"><span data-stu-id="22de3-536">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22de3-537"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22de3-537"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22de3-538">DLL</span><span class="sxs-lookup"><span data-stu-id="22de3-538">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22de3-539"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22de3-539"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22de3-540">Confira também</span><span class="sxs-lookup"><span data-stu-id="22de3-540">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22de3-541">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="22de3-541">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

