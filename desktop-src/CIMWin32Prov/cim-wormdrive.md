---
description: A \_ classe CIM WORMDrive representa os recursos e o gerenciamento de uma unidade de worm, um subtipo do dispositivo de acesso à mídia.
ms.assetid: df77084a-01f2-4cca-b395-d74ee64ef526
ms.tgt_platform: multiple
title: Classe CIM_WORMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WORMDrive
- CIM_WORMDrive.Availability
- CIM_WORMDrive.Capabilities
- CIM_WORMDrive.CapabilityDescriptions
- CIM_WORMDrive.Caption
- CIM_WORMDrive.CompressionMethod
- CIM_WORMDrive.ConfigManagerErrorCode
- CIM_WORMDrive.ConfigManagerUserConfig
- CIM_WORMDrive.CreationClassName
- CIM_WORMDrive.DefaultBlockSize
- CIM_WORMDrive.Description
- CIM_WORMDrive.DeviceID
- CIM_WORMDrive.ErrorCleared
- CIM_WORMDrive.ErrorDescription
- CIM_WORMDrive.ErrorMethodology
- CIM_WORMDrive.InstallDate
- CIM_WORMDrive.LastErrorCode
- CIM_WORMDrive.MaxBlockSize
- CIM_WORMDrive.MaxMediaSize
- CIM_WORMDrive.MinBlockSize
- CIM_WORMDrive.Name
- CIM_WORMDrive.NeedsCleaning
- CIM_WORMDrive.NumberOfMediaSupported
- CIM_WORMDrive.PNPDeviceID
- CIM_WORMDrive.PowerManagementCapabilities
- CIM_WORMDrive.PowerManagementSupported
- CIM_WORMDrive.Status
- CIM_WORMDrive.StatusInfo
- CIM_WORMDrive.SystemCreationClassName
- CIM_WORMDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 08133d1abdcb6fc401ee4ad730d82ef97fb30200
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088979"
---
# <a name="cim_wormdrive-class"></a><span data-ttu-id="3e9cd-103">\_Classe CIM WORMDrive</span><span class="sxs-lookup"><span data-stu-id="3e9cd-103">CIM\_WORMDrive class</span></span>

<span data-ttu-id="3e9cd-104">A classe **CIM \_ WORMDrive** representa os recursos e o gerenciamento de uma unidade de worm, um subtipo do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-104">The **CIM\_WORMDrive** class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e9cd-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e9cd-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e9cd-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3e9cd-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9cd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e9cd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FFB58B9A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_WORMDrive : CIM_MediaAccessDevice
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="3e9cd-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3e9cd-110">Members</span></span>

<span data-ttu-id="3e9cd-111">A classe **CIM \_ WORMDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3e9cd-111">The **CIM\_WORMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="3e9cd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3e9cd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3e9cd-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e9cd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3e9cd-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="3e9cd-114">Methods</span></span>

<span data-ttu-id="3e9cd-115">A classe **CIM \_ WORMDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-115">The **CIM\_WORMDrive** class has these methods.</span></span>



| <span data-ttu-id="3e9cd-116">Método</span><span class="sxs-lookup"><span data-stu-id="3e9cd-116">Method</span></span>                                                               | <span data-ttu-id="3e9cd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e9cd-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e9cd-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-118">**Reset**</span></span>](reset-method-in-class-cim-wormdrive.md)                 | <span data-ttu-id="3e9cd-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="3e9cd-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="3e9cd-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-wormdrive.md) | <span data-ttu-id="3e9cd-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="3e9cd-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3e9cd-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3e9cd-124">Properties</span></span>

<span data-ttu-id="3e9cd-125">A classe **CIM \_ WORMDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-125">The **CIM\_WORMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e9cd-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-130">Availability and status of the device.</span></span>

<span data-ttu-id="3e9cd-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3e9cd-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e9cd-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3e9cd-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-135">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="3e9cd-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3e9cd-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3e9cd-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3e9cd-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3e9cd-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="3e9cd-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3e9cd-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3e9cd-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3e9cd-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3e9cd-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3e9cd-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3e9cd-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-146">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3e9cd-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-148">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3e9cd-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-150">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3e9cd-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3e9cd-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-153">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3e9cd-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-155">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3e9cd-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-157">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3e9cd-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-159">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3e9cd-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-161">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-162">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-163">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-165">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-166">Recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-166">Capabilities of the media access device.</span></span> <span data-ttu-id="3e9cd-167">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e9cd-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3e9cd-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="3e9cd-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="3e9cd-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="3e9cd-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="3e9cd-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="3e9cd-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="3e9cd-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-176">Mídia removível.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-176">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="3e9cd-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="3e9cd-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="3e9cd-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="3e9cd-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-181">Distingue um dispositivo que pode acessar ambos os lados da mídia de dois lados de um dispositivo que lê apenas um único lado e requer que a mídia seja transferida.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-181">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="3e9cd-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-183">Indica que a mídia não precisa ser desejetada explicitamente do dispositivo antes de ser acessada por um elemento de seletor.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-183">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-185">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-187">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-187">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-188">Cadeias de caracteres de forma livre que fornecem descrições detalhadas para os recursos de dispositivo de acesso indicados na matriz de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="3e9cd-188">Free-form strings that provide detailed descriptions for the access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="3e9cd-189">Cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-189">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="3e9cd-190">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-190">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-191">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-192">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-194">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-195">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-195">Short textual description of the object.</span></span>

<span data-ttu-id="3e9cd-196">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-197">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-197">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-198">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-200">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-200">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="3e9cd-201">Se o esquema de compactação for desconhecido ou não estiver descrito, use "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="3e9cd-201">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="3e9cd-202">Se o arquivo lógico estiver compactado, mas o esquema de compactação for desconhecido ou não estiver descrito, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="3e9cd-202">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="3e9cd-203">Se o arquivo lógico não estiver compactado, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="3e9cd-203">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="3e9cd-204">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-204">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="3e9cd-205">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-206">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-206">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="3e9cd-207">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-208">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="3e9cd-208">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="3e9cd-209">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-210">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="3e9cd-210">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-212">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-214">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-215">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="3e9cd-216">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3e9cd-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3e9cd-218"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-219">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3e9cd-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3e9cd-221">(1)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-222">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3e9cd-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3e9cd-224">(2)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3e9cd-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3e9cd-226">(3)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-227">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3e9cd-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3e9cd-229">(4)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-230">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-230">Device is not working properly.</span></span> <span data-ttu-id="3e9cd-231">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3e9cd-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3e9cd-233">(5)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-234">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3e9cd-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3e9cd-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-237">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3e9cd-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3e9cd-239">(7)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3e9cd-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3e9cd-241">(8)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-242">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3e9cd-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3e9cd-244">(9)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-245">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-245">Device is not working properly.</span></span> <span data-ttu-id="3e9cd-246">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3e9cd-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3e9cd-248">(10)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-249">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3e9cd-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3e9cd-251">(11)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-252">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3e9cd-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3e9cd-254">12</span><span class="sxs-lookup"><span data-stu-id="3e9cd-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-255">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3e9cd-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3e9cd-257">(13)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-258">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3e9cd-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3e9cd-260">(14)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-261">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3e9cd-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3e9cd-263">(15)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-264">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3e9cd-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3e9cd-266">(16)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-267">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3e9cd-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3e9cd-269">(17)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-270">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3e9cd-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3e9cd-272">(18)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-273">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3e9cd-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3e9cd-275">(19)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3e9cd-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3e9cd-277">(20)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-278">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3e9cd-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3e9cd-280">(21)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-281">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-281">System failure.</span></span> <span data-ttu-id="3e9cd-282">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3e9cd-283">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3e9cd-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3e9cd-285">(22)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-286">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3e9cd-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3e9cd-288">(23)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-289">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-289">System failure.</span></span> <span data-ttu-id="3e9cd-290">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3e9cd-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3e9cd-292">(24)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-293">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3e9cd-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3e9cd-295">(25)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-296">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3e9cd-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3e9cd-298">(26)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-299">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3e9cd-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3e9cd-301">(27)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-302">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3e9cd-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3e9cd-304">(28)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-305">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3e9cd-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3e9cd-307">(29)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-308">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-308">Device is disabled.</span></span> <span data-ttu-id="3e9cd-309">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3e9cd-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3e9cd-311">(30)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-312">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3e9cd-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3e9cd-314">(31)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-315">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-315">Device is not working properly.</span></span> <span data-ttu-id="3e9cd-316">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-318">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-320">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-321">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-321">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3e9cd-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-326">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-327">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-327">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3e9cd-328">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-328">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3e9cd-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-330">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-331">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-333">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-334">Tamanho de bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-334">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="3e9cd-335">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3e9cd-336">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-337">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-338">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-339">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-340">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-341">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-341">Textual description of the object.</span></span>

<span data-ttu-id="3e9cd-342">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-344">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-346">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-346">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-347">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-347">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="3e9cd-348">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-350">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-352">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-352">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="3e9cd-353">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-357">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-357">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="3e9cd-358">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-362">Cadeia de caracteres de forma livre que descreve os tipos de detecção de erro e correção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-362">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="3e9cd-363">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-364">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-364">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-365">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-367">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-368">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-368">Date and time the object was installed.</span></span> <span data-ttu-id="3e9cd-369">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-369">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3e9cd-370">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-371">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-371">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-372">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-372">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-374">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-374">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3e9cd-375">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-376">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-376">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-377">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-379">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-379">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-380">Tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-380">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="3e9cd-381">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-381">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3e9cd-382">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-382">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-383">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-383">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-384">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-384">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-386">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-387">Tamanho máximo, em quilobytes, de mídia com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-387">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="3e9cd-388">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-388">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="3e9cd-389">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3e9cd-390">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-391">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-391">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-392">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-394">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-395">Tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-395">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="3e9cd-396">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3e9cd-397">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-398">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-398">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-401">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-401">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-402">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-402">Label by which the object is known.</span></span> <span data-ttu-id="3e9cd-403">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-403">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="3e9cd-404">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-405">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-405">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-406">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-408">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-408">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="3e9cd-409">A limpeza manual ou automática é possível é indicada na propriedade da matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="3e9cd-409">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="3e9cd-410">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-410">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-411">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-411">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-412">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-414">Quando o dispositivo de acesso à mídia dá suporte a várias mídias individuais, essa propriedade define o número máximo que pode ser suportado ou inserido.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-414">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="3e9cd-415">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-415">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-416">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-416">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-417">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-419">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-419">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-420">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-420">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="3e9cd-421">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3e9cd-422">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3e9cd-422">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-423">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-423">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-424">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-424">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-426">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-426">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3e9cd-427">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-427">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e9cd-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3e9cd-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-430">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-430">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3e9cd-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3e9cd-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-433">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-433">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3e9cd-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-435">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-435">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3e9cd-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-437">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="3e9cd-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3e9cd-438">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-438">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="3e9cd-439">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-439">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3e9cd-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-441">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-441">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3e9cd-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3e9cd-443">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-444">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-444">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-445">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-445">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-447">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-447">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="3e9cd-448">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="3e9cd-448">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="3e9cd-449">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-449">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="3e9cd-450">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="3e9cd-450">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="3e9cd-451">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-452">**Status**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-452">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-453">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-455">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-455">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-456">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-456">Current status of the object.</span></span> <span data-ttu-id="3e9cd-457">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3e9cd-458">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3e9cd-458">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3e9cd-459">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-459">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3e9cd-460">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-460">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3e9cd-461">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-461">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e9cd-462">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-462">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3e9cd-463">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-463">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3e9cd-464">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-464">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3e9cd-465">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-465">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3e9cd-466">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-466">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3e9cd-467">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-467">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3e9cd-468">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-468">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3e9cd-469">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-469">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3e9cd-470">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-470">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-471">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-471">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-472">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-474">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="3e9cd-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-475">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-475">State of the logical device.</span></span> <span data-ttu-id="3e9cd-476">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-476">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3e9cd-477">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3e9cd-478">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-478">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3e9cd-479">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-479">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3e9cd-480">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-480">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3e9cd-481">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-481">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3e9cd-482">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-482">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e9cd-483">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-483">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-484">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-485">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-486">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-486">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-487">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-487">Scoping system's creation class name.</span></span>

<span data-ttu-id="3e9cd-488">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-488">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e9cd-489">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-489">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9cd-490">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-491">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3e9cd-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9cd-492">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3e9cd-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3e9cd-493">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-493">Scoping system's name.</span></span>

<span data-ttu-id="3e9cd-494">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e9cd-495">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e9cd-495">Remarks</span></span>

<span data-ttu-id="3e9cd-496">A classe **CIM \_ WORMDrive** é derivada de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="3e9cd-496">The **CIM\_WORMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3e9cd-497">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-497">WMI does not implement this class.</span></span>

<span data-ttu-id="3e9cd-498">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-498">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e9cd-499">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3e9cd-499">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9cd-500">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e9cd-500">Requirements</span></span>



| <span data-ttu-id="3e9cd-501">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e9cd-501">Requirement</span></span> | <span data-ttu-id="3e9cd-502">Valor</span><span class="sxs-lookup"><span data-stu-id="3e9cd-502">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9cd-503">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e9cd-503">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9cd-504">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e9cd-504">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e9cd-505">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e9cd-505">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9cd-506">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e9cd-506">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e9cd-507">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e9cd-507">Namespace</span></span><br/>                | <span data-ttu-id="3e9cd-508">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3e9cd-508">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e9cd-509">MOF</span><span class="sxs-lookup"><span data-stu-id="3e9cd-509">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e9cd-510"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e9cd-510"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e9cd-511">DLL</span><span class="sxs-lookup"><span data-stu-id="3e9cd-511">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e9cd-512"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e9cd-512"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9cd-513">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e9cd-513">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9cd-514">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3e9cd-514">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

