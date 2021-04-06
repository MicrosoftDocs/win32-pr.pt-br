---
description: A \_ classe CIM CDROMDrive representa uma unidade de CD-ROM no computador.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: Classe CIM_CDROMDrive (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826506"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="147a6-103">Classe CIM_CDROMDrive (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="147a6-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="147a6-104">A classe **CIM \_ CDROMDrive** representa uma unidade de CD-ROM no computador.</span><span class="sxs-lookup"><span data-stu-id="147a6-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="147a6-105">O nome da unidade não corresponde à letra da unidade lógica atribuída ao dispositivo, que é o nome do dispositivo de armazenamento lógico dependente da unidade.</span><span class="sxs-lookup"><span data-stu-id="147a6-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="147a6-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="147a6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="147a6-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="147a6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="147a6-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="147a6-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="147a6-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="147a6-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="147a6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="147a6-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="147a6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="147a6-111">Members</span></span>

<span data-ttu-id="147a6-112">A classe **CIM \_ CDROMDrive** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="147a6-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="147a6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="147a6-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="147a6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="147a6-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="147a6-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="147a6-115">Methods</span></span>

<span data-ttu-id="147a6-116">A classe **CIM \_ CDROMDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="147a6-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="147a6-117">Método</span><span class="sxs-lookup"><span data-stu-id="147a6-117">Method</span></span>                                                                | <span data-ttu-id="147a6-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="147a6-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="147a6-119">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="147a6-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="147a6-120">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="147a6-121">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="147a6-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="147a6-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="147a6-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="147a6-123">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="147a6-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="147a6-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="147a6-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="147a6-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="147a6-125">Properties</span></span>

<span data-ttu-id="147a6-126">A classe **CIM \_ CDROMDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="147a6-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="147a6-127">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="147a6-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-128">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="147a6-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="147a6-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-131">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-131">Availability and status of the device.</span></span>

<span data-ttu-id="147a6-132">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="147a6-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="147a6-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="147a6-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="147a6-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="147a6-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="147a6-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="147a6-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="147a6-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="147a6-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="147a6-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="147a6-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="147a6-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="147a6-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="147a6-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="147a6-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="147a6-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="147a6-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="147a6-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="147a6-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="147a6-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="147a6-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="147a6-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="147a6-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="147a6-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="147a6-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="147a6-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-146">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="147a6-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="147a6-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="147a6-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-148">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="147a6-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="147a6-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="147a6-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-150">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="147a6-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="147a6-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="147a6-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="147a6-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="147a6-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-153">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="147a6-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="147a6-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="147a6-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-155">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="147a6-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="147a6-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="147a6-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-157">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="147a6-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="147a6-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="147a6-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-159">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="147a6-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="147a6-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="147a6-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-161">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="147a6-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-162">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="147a6-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-163">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="147a6-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="147a6-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-165">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="147a6-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-166">Recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="147a6-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="147a6-167">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="147a6-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="147a6-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-169">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="147a6-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="147a6-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="147a6-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-171">Outros.</span><span class="sxs-lookup"><span data-stu-id="147a6-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="147a6-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="147a6-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-173">Acesso sequencial.</span><span class="sxs-lookup"><span data-stu-id="147a6-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="147a6-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="147a6-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-175">Acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="147a6-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="147a6-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="147a6-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-177">Criando.</span><span class="sxs-lookup"><span data-stu-id="147a6-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="147a6-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="147a6-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-179">Criptografia.</span><span class="sxs-lookup"><span data-stu-id="147a6-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="147a6-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="147a6-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-181">Compactação.</span><span class="sxs-lookup"><span data-stu-id="147a6-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="147a6-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="147a6-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-183">Mídia removível.</span><span class="sxs-lookup"><span data-stu-id="147a6-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="147a6-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="147a6-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-185">Limpeza manual.</span><span class="sxs-lookup"><span data-stu-id="147a6-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="147a6-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="147a6-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-187">Limpeza automática.</span><span class="sxs-lookup"><span data-stu-id="147a6-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="147a6-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="147a6-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-189">Notificação inteligente.</span><span class="sxs-lookup"><span data-stu-id="147a6-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="147a6-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="147a6-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-191">Distingue um dispositivo que pode acessar ambos os lados da mídia de dois lados de um dispositivo que lê apenas um único lado e requer que a mídia seja transferida.</span><span class="sxs-lookup"><span data-stu-id="147a6-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="147a6-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="147a6-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-193">Indica que a mídia não precisa ser desejetada explicitamente do dispositivo antes de ser acessada por um elemento de seletor.</span><span class="sxs-lookup"><span data-stu-id="147a6-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-194">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="147a6-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-195">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="147a6-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-197">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="147a6-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-198">Matriz de cadeias de caracteres de forma livre que fornece explicações detalhadas para acessar recursos do dispositivo indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="147a6-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="147a6-199">Cada entrada dessa matriz está relacionada à entrada na matriz **Capabilities** , localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="147a6-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="147a6-200">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-201">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="147a6-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-204">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="147a6-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-205">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="147a6-205">A short textual description of the object.</span></span>

<span data-ttu-id="147a6-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="147a6-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-210">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="147a6-211">Se não for possível descrever o esquema de compactação (porque ele é desconhecido), use o seguinte: If, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="147a6-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="147a6-212">Se, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="147a6-212">If , use "Compressed".</span></span> <span data-ttu-id="147a6-213">, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="147a6-213">, use "Not Compressed".</span></span>

<span data-ttu-id="147a6-214">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="147a6-215">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="147a6-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="147a6-216">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="147a6-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="147a6-217">("Compactado")</span><span class="sxs-lookup"><span data-stu-id="147a6-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="147a6-218">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="147a6-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="147a6-219">("Não compactado")</span><span class="sxs-lookup"><span data-stu-id="147a6-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="147a6-220">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="147a6-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-221">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="147a6-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-222">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="147a6-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-224">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="147a6-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-225">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="147a6-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="147a6-226">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="147a6-227">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="147a6-227">**This device is working properly.**</span></span> <span data-ttu-id="147a6-228"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="147a6-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="147a6-229">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="147a6-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="147a6-230">(1)</span><span class="sxs-lookup"><span data-stu-id="147a6-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="147a6-231">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="147a6-232">(2)</span><span class="sxs-lookup"><span data-stu-id="147a6-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="147a6-233">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="147a6-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="147a6-234">(3)</span><span class="sxs-lookup"><span data-stu-id="147a6-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="147a6-235">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="147a6-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="147a6-236">(4)</span><span class="sxs-lookup"><span data-stu-id="147a6-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="147a6-237">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="147a6-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="147a6-238">(5)</span><span class="sxs-lookup"><span data-stu-id="147a6-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="147a6-239">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="147a6-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="147a6-240"> (6)</span><span class="sxs-lookup"><span data-stu-id="147a6-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="147a6-241">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="147a6-241">**Cannot filter.**</span></span> <span data-ttu-id="147a6-242">(7)</span><span class="sxs-lookup"><span data-stu-id="147a6-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="147a6-243">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="147a6-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="147a6-244">(8)</span><span class="sxs-lookup"><span data-stu-id="147a6-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="147a6-245">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="147a6-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="147a6-246">(9)</span><span class="sxs-lookup"><span data-stu-id="147a6-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="147a6-247">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="147a6-247">**This device cannot start.**</span></span> <span data-ttu-id="147a6-248">(10)</span><span class="sxs-lookup"><span data-stu-id="147a6-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="147a6-249">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="147a6-249">**This device failed.**</span></span> <span data-ttu-id="147a6-250">(11)</span><span class="sxs-lookup"><span data-stu-id="147a6-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="147a6-251">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="147a6-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="147a6-252">12</span><span class="sxs-lookup"><span data-stu-id="147a6-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="147a6-253">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="147a6-254">(13)</span><span class="sxs-lookup"><span data-stu-id="147a6-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="147a6-255">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="147a6-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="147a6-256">(14)</span><span class="sxs-lookup"><span data-stu-id="147a6-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="147a6-257">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="147a6-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="147a6-258">(15)</span><span class="sxs-lookup"><span data-stu-id="147a6-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="147a6-259">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="147a6-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="147a6-260">(16)</span><span class="sxs-lookup"><span data-stu-id="147a6-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="147a6-261">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="147a6-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="147a6-262">(17)</span><span class="sxs-lookup"><span data-stu-id="147a6-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="147a6-263">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="147a6-264">(18)</span><span class="sxs-lookup"><span data-stu-id="147a6-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="147a6-265">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="147a6-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="147a6-266">(19)</span><span class="sxs-lookup"><span data-stu-id="147a6-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="147a6-267">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="147a6-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="147a6-268">(20)</span><span class="sxs-lookup"><span data-stu-id="147a6-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="147a6-269">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="147a6-270">(21)</span><span class="sxs-lookup"><span data-stu-id="147a6-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="147a6-271">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="147a6-271">**This device is disabled.**</span></span> <span data-ttu-id="147a6-272">(22)</span><span class="sxs-lookup"><span data-stu-id="147a6-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="147a6-273">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="147a6-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="147a6-274">(23)</span><span class="sxs-lookup"><span data-stu-id="147a6-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="147a6-275">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="147a6-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="147a6-276">(24)</span><span class="sxs-lookup"><span data-stu-id="147a6-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="147a6-277">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="147a6-278">(25)</span><span class="sxs-lookup"><span data-stu-id="147a6-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="147a6-279">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="147a6-280">(26)</span><span class="sxs-lookup"><span data-stu-id="147a6-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="147a6-281">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="147a6-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="147a6-282">(27)</span><span class="sxs-lookup"><span data-stu-id="147a6-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="147a6-283">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="147a6-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="147a6-284">(28)</span><span class="sxs-lookup"><span data-stu-id="147a6-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="147a6-285">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="147a6-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="147a6-286">(29)</span><span class="sxs-lookup"><span data-stu-id="147a6-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="147a6-287">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="147a6-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="147a6-288">(30)</span><span class="sxs-lookup"><span data-stu-id="147a6-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="147a6-289">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="147a6-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="147a6-290">(31)</span><span class="sxs-lookup"><span data-stu-id="147a6-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="147a6-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-292">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="147a6-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-293">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-294">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="147a6-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-295">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="147a6-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="147a6-296">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="147a6-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-298">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-299">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-300">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="147a6-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="147a6-301">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="147a6-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="147a6-302">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="147a6-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="147a6-303">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-304">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="147a6-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-305">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="147a6-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-307">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="147a6-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-308">Tamanho de bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="147a6-309">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="147a6-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="147a6-310">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-311">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="147a6-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-312">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-313">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-314">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="147a6-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-315">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="147a6-315">A textual description of the object.</span></span>

<span data-ttu-id="147a6-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="147a6-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-318">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-320">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="147a6-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="147a6-321">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="147a6-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="147a6-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-324">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="147a6-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-326">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="147a6-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="147a6-327">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="147a6-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-331">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="147a6-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="147a6-332">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-333">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="147a6-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-334">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-336">Cadeia de caracteres de forma livre que descreve os tipos de detecção de erro e correção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="147a6-337">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="147a6-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-339">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="147a6-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-341">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="147a6-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-342">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="147a6-342">Indicates when the object was installed.</span></span> <span data-ttu-id="147a6-343">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="147a6-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="147a6-344">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="147a6-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-346">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="147a6-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-348">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="147a6-349">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-350">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="147a6-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-351">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="147a6-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-352">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-353">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="147a6-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-354">Tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="147a6-355">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="147a6-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="147a6-356">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-357">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="147a6-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-358">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="147a6-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-360">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="147a6-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-361">Tamanho máximo, em quilobytes, de mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="147a6-362">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="147a6-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="147a6-363">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="147a6-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="147a6-364">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-365">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="147a6-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-366">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="147a6-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-368">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="147a6-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-369">Tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="147a6-370">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="147a6-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="147a6-371">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-372">**Nome**</span><span class="sxs-lookup"><span data-stu-id="147a6-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-373">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-375">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="147a6-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-376">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="147a6-376">Label by which the object is known.</span></span> <span data-ttu-id="147a6-377">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="147a6-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="147a6-378">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-379">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="147a6-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-380">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="147a6-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-381">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-382">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="147a6-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="147a6-383">A limpeza manual ou automática é possível é indicada na propriedade da matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="147a6-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="147a6-384">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-385">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="147a6-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-386">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="147a6-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-388">Número máximo de várias mídias individuais que podem ser suportadas ou inseridas.</span><span class="sxs-lookup"><span data-stu-id="147a6-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="147a6-389">Essa propriedade é herdada do [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="147a6-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-391">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-392">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-393">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="147a6-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-394">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="147a6-395">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="147a6-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="147a6-396">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-397">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="147a6-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-398">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="147a6-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="147a6-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-400">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="147a6-401">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="147a6-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="147a6-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-403">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="147a6-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="147a6-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="147a6-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-405">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="147a6-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="147a6-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="147a6-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-407">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="147a6-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="147a6-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="147a6-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-409">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="147a6-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="147a6-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="147a6-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-411">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="147a6-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="147a6-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="147a6-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-413">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="147a6-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="147a6-414">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="147a6-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="147a6-415">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="147a6-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="147a6-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="147a6-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-417">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="147a6-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="147a6-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="147a6-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="147a6-419">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="147a6-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-420">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="147a6-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-421">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="147a6-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-422">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="147a6-423">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="147a6-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="147a6-424">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="147a6-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="147a6-425">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="147a6-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="147a6-426">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="147a6-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="147a6-427">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-428">**Status**</span><span class="sxs-lookup"><span data-stu-id="147a6-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-429">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-431">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="147a6-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-432">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="147a6-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="147a6-433">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="147a6-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="147a6-434">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="147a6-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="147a6-435">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="147a6-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="147a6-436">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="147a6-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="147a6-437">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="147a6-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="147a6-438">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="147a6-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="147a6-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="147a6-440">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="147a6-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="147a6-441">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="147a6-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="147a6-442">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="147a6-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="147a6-443">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="147a6-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="147a6-444">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="147a6-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="147a6-445">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="147a6-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="147a6-446">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="147a6-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="147a6-447">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="147a6-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="147a6-448">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="147a6-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="147a6-449">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="147a6-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="147a6-450">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="147a6-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="147a6-451">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="147a6-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="147a6-452">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="147a6-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="147a6-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-454">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="147a6-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-456">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="147a6-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="147a6-457">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="147a6-457">State of the logical device.</span></span> <span data-ttu-id="147a6-458">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="147a6-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="147a6-459">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="147a6-460">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="147a6-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="147a6-461">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="147a6-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="147a6-462">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="147a6-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="147a6-463">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="147a6-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="147a6-464">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="147a6-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="147a6-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="147a6-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-466">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-467">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-468">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="147a6-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="147a6-469">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="147a6-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="147a6-470">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="147a6-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="147a6-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="147a6-472">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="147a6-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="147a6-473">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="147a6-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="147a6-474">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="147a6-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="147a6-475">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="147a6-475">The scoping system's name.</span></span>

<span data-ttu-id="147a6-476">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="147a6-477">Comentários</span><span class="sxs-lookup"><span data-stu-id="147a6-477">Remarks</span></span>

<span data-ttu-id="147a6-478">A classe **CIM \_ CDROMDrive** é derivada de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="147a6-479">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="147a6-479">WMI does not implement this class.</span></span> <span data-ttu-id="147a6-480">Para obter mais informações sobre classes derivadas de **CIM \_ CDROMDrive**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="147a6-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="147a6-481">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="147a6-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="147a6-482">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="147a6-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="147a6-483">Requisitos</span><span class="sxs-lookup"><span data-stu-id="147a6-483">Requirements</span></span>



| <span data-ttu-id="147a6-484">Requisito</span><span class="sxs-lookup"><span data-stu-id="147a6-484">Requirement</span></span> | <span data-ttu-id="147a6-485">Valor</span><span class="sxs-lookup"><span data-stu-id="147a6-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147a6-486">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="147a6-486">Minimum supported client</span></span><br/> | <span data-ttu-id="147a6-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="147a6-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="147a6-488">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="147a6-488">Minimum supported server</span></span><br/> | <span data-ttu-id="147a6-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="147a6-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="147a6-490">Namespace</span><span class="sxs-lookup"><span data-stu-id="147a6-490">Namespace</span></span><br/>                | <span data-ttu-id="147a6-491">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="147a6-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="147a6-492">MOF</span><span class="sxs-lookup"><span data-stu-id="147a6-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="147a6-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="147a6-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="147a6-494">DLL</span><span class="sxs-lookup"><span data-stu-id="147a6-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="147a6-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="147a6-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="147a6-496">Confira também</span><span class="sxs-lookup"><span data-stu-id="147a6-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="147a6-497">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="147a6-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

