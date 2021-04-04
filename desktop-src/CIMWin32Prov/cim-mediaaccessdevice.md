---
description: A \_ classe CIM MediaAccessDevice representa a capacidade de acessar uma ou mais mídias e, em seguida, usar a mídia para armazenar e recuperar dados.
ms.assetid: 224a7b08-1566-4b0b-90d8-9991fa188d93
ms.tgt_platform: multiple
title: Classe CIM_MediaAccessDevice (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Caption
- CIM_MediaAccessDevice.Description
- CIM_MediaAccessDevice.InstallDate
- CIM_MediaAccessDevice.Name
- CIM_MediaAccessDevice.Status
- CIM_MediaAccessDevice.Availability
- CIM_MediaAccessDevice.ConfigManagerErrorCode
- CIM_MediaAccessDevice.ConfigManagerUserConfig
- CIM_MediaAccessDevice.CreationClassName
- CIM_MediaAccessDevice.DeviceID
- CIM_MediaAccessDevice.PowerManagementCapabilities
- CIM_MediaAccessDevice.ErrorCleared
- CIM_MediaAccessDevice.ErrorDescription
- CIM_MediaAccessDevice.LastErrorCode
- CIM_MediaAccessDevice.PNPDeviceID
- CIM_MediaAccessDevice.PowerManagementSupported
- CIM_MediaAccessDevice.StatusInfo
- CIM_MediaAccessDevice.SystemCreationClassName
- CIM_MediaAccessDevice.SystemName
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de0b993b4cc1da46b19b1c296fae44e855c5816
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837674"
---
# <a name="cim_mediaaccessdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="240a4-103">Classe CIM_MediaAccessDevice (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="240a4-103">CIM_MediaAccessDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="240a4-104">A classe **CIM \_ MediaAccessDevice** representa a capacidade de acessar uma ou mais mídias e, em seguida, usar a mídia para armazenar e recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="240a4-104">The **CIM\_MediaAccessDevice** class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="240a4-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="240a4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="240a4-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="240a4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="240a4-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="240a4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="240a4-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="240a4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="240a4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="240a4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
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

## <a name="members"></a><span data-ttu-id="240a4-110">Membros</span><span class="sxs-lookup"><span data-stu-id="240a4-110">Members</span></span>

<span data-ttu-id="240a4-111">A classe **CIM \_ MediaAccessDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="240a4-111">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="240a4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="240a4-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="240a4-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="240a4-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="240a4-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="240a4-114">Methods</span></span>

<span data-ttu-id="240a4-115">A classe **CIM \_ MediaAccessDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="240a4-115">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="240a4-116">Método</span><span class="sxs-lookup"><span data-stu-id="240a4-116">Method</span></span>                                                                       | <span data-ttu-id="240a4-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="240a4-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="240a4-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="240a4-118">**Reset**</span></span>](reset-method-in-class-cim-mediaaccessdevice.md)                 | <span data-ttu-id="240a4-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="240a4-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="240a4-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="240a4-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="240a4-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-mediaaccessdevice.md) | <span data-ttu-id="240a4-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="240a4-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="240a4-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="240a4-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="240a4-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="240a4-124">Properties</span></span>

<span data-ttu-id="240a4-125">A classe **CIM \_ MediaAccessDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="240a4-125">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="240a4-126">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="240a4-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="240a4-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-129">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="240a4-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-130">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-130">Availability and status of the device.</span></span>

<span data-ttu-id="240a4-131">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="240a4-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="240a4-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="240a4-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="240a4-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="240a4-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="240a4-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="240a4-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="240a4-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="240a4-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="240a4-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="240a4-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="240a4-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="240a4-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="240a4-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="240a4-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="240a4-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="240a4-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="240a4-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="240a4-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="240a4-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="240a4-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="240a4-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="240a4-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="240a4-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="240a4-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="240a4-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-145">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="240a4-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="240a4-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="240a4-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-147">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="240a4-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="240a4-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="240a4-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-149">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="240a4-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="240a4-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="240a4-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="240a4-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="240a4-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-152">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="240a4-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="240a4-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="240a4-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-154">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="240a4-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="240a4-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="240a4-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-156">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="240a4-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="240a4-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="240a4-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-158">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="240a4-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="240a4-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="240a4-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-160">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="240a4-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-161">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="240a4-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-162">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="240a4-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="240a4-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-164">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de armazenamento DMTF \| 1,9 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,11 "," MIF. \|Dispositivos de armazenamento DMTF \| 1,12 "," MIF. \|Discos DMTF \| 3,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="240a4-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-165">Recursos do dispositivo de acesso à mídia.</span><span class="sxs-lookup"><span data-stu-id="240a4-165">Capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="240a4-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="240a4-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-167">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="240a4-167">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="240a4-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="240a4-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-169">Outros.</span><span class="sxs-lookup"><span data-stu-id="240a4-169">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="240a4-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acesso sequencial** (2)</span><span class="sxs-lookup"><span data-stu-id="240a4-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-171">Acesso sequencial.</span><span class="sxs-lookup"><span data-stu-id="240a4-171">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="240a4-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acesso aleatório** (3)</span><span class="sxs-lookup"><span data-stu-id="240a4-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-173">Acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="240a4-173">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="240a4-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Dá suporte à gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="240a4-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-175">Criando.</span><span class="sxs-lookup"><span data-stu-id="240a4-175">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="240a4-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Criptografia** (5)</span><span class="sxs-lookup"><span data-stu-id="240a4-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-177">Criptografia.</span><span class="sxs-lookup"><span data-stu-id="240a4-177">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="240a4-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compactação** (6)</span><span class="sxs-lookup"><span data-stu-id="240a4-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-179">Compactação.</span><span class="sxs-lookup"><span data-stu-id="240a4-179">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="240a4-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Dá suporte à mídia removida** (7)</span><span class="sxs-lookup"><span data-stu-id="240a4-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-181">Mídia removível.</span><span class="sxs-lookup"><span data-stu-id="240a4-181">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="240a4-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpeza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="240a4-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-183">Limpeza manual.</span><span class="sxs-lookup"><span data-stu-id="240a4-183">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="240a4-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpeza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="240a4-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-185">Limpeza automática.</span><span class="sxs-lookup"><span data-stu-id="240a4-185">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="240a4-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificação inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="240a4-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-187">Notificação inteligente.</span><span class="sxs-lookup"><span data-stu-id="240a4-187">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="240a4-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Dá suporte à mídia de dois lados** (11)</span><span class="sxs-lookup"><span data-stu-id="240a4-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-189">Mídia de dois lados.</span><span class="sxs-lookup"><span data-stu-id="240a4-189">Dual-sided media.</span></span>

<span data-ttu-id="240a4-190">Distingue um dispositivo que pode acessar ambos os lados da mídia de dois lados de um dispositivo que lê apenas um único lado e requer que a mídia seja transferida.</span><span class="sxs-lookup"><span data-stu-id="240a4-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="240a4-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Ejeção de desmontagem não necessária** (12)</span><span class="sxs-lookup"><span data-stu-id="240a4-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-192">Indica que a mídia não precisa ser desejetada explicitamente do dispositivo antes de ser acessada por um elemento de seletor.</span><span class="sxs-lookup"><span data-stu-id="240a4-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-193">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="240a4-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-194">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="240a4-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-196">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MediaAccessDevice**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="240a4-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-197">Matriz de cadeias de caracteres de forma livre que fornece explicações detalhadas para acessar recursos do dispositivo indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="240a4-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="240a4-198">Cada entrada dessa matriz está relacionada à entrada na matriz **Capabilities** , localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="240a4-198">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="240a4-199">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="240a4-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-202">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="240a4-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-203">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="240a4-203">A short textual description of the object.</span></span>

<span data-ttu-id="240a4-204">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-205">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="240a4-205">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-206">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-208">Cadeia de caracteres de forma livre que indica o algoritmo ou a ferramenta usada para compactar o arquivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="240a4-209">Se não for possível descrever o esquema de compactação (porque ele é desconhecido), use o seguinte: If, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="240a4-209">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="240a4-210">Se, use "compactado".</span><span class="sxs-lookup"><span data-stu-id="240a4-210">If , use "Compressed".</span></span> <span data-ttu-id="240a4-211">, use "não compactado".</span><span class="sxs-lookup"><span data-stu-id="240a4-211">, use "Not Compressed".</span></span>

<dt>

<span data-ttu-id="240a4-212">Conhecidos</span><span class="sxs-lookup"><span data-stu-id="240a4-212">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="240a4-213">O esquema de compactação é desconhecido ou não está descrito.</span><span class="sxs-lookup"><span data-stu-id="240a4-213">The compression scheme is unknown or not described.</span></span>

</dd> <dt>

<span data-ttu-id="240a4-214">Compactados</span><span class="sxs-lookup"><span data-stu-id="240a4-214">"Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="240a4-215">O arquivo lógico está compactado, mas o esquema de compactação é desconhecido ou não está descrito</span><span class="sxs-lookup"><span data-stu-id="240a4-215">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>

<span data-ttu-id="240a4-216">"Não compactado"</span><span class="sxs-lookup"><span data-stu-id="240a4-216">"Not Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="240a4-217">Se o arquivo lógico não for compactado</span><span class="sxs-lookup"><span data-stu-id="240a4-217">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-218">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="240a4-218">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-219">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a4-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-221">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="240a4-221">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-222">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="240a4-222">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="240a4-223">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-223">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="240a4-224">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="240a4-224">**This device is working properly.**</span></span> <span data-ttu-id="240a4-225"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="240a4-225">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="240a4-226">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="240a4-226">**This device is not configured correctly.**</span></span> <span data-ttu-id="240a4-227">(1)</span><span class="sxs-lookup"><span data-stu-id="240a4-227">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="240a4-228">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-228">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="240a4-229">(2)</span><span class="sxs-lookup"><span data-stu-id="240a4-229">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="240a4-230">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="240a4-230">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="240a4-231">(3)</span><span class="sxs-lookup"><span data-stu-id="240a4-231">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="240a4-232">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="240a4-232">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="240a4-233">(4)</span><span class="sxs-lookup"><span data-stu-id="240a4-233">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="240a4-234">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="240a4-234">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="240a4-235">(5)</span><span class="sxs-lookup"><span data-stu-id="240a4-235">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="240a4-236">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="240a4-236">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="240a4-237"> (6)</span><span class="sxs-lookup"><span data-stu-id="240a4-237">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="240a4-238">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="240a4-238">**Cannot filter.**</span></span> <span data-ttu-id="240a4-239">(7)</span><span class="sxs-lookup"><span data-stu-id="240a4-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="240a4-240">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="240a4-240">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="240a4-241">(8)</span><span class="sxs-lookup"><span data-stu-id="240a4-241">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="240a4-242">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="240a4-242">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="240a4-243">(9)</span><span class="sxs-lookup"><span data-stu-id="240a4-243">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="240a4-244">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="240a4-244">**This device cannot start.**</span></span> <span data-ttu-id="240a4-245">(10)</span><span class="sxs-lookup"><span data-stu-id="240a4-245">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="240a4-246">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="240a4-246">**This device failed.**</span></span> <span data-ttu-id="240a4-247">(11)</span><span class="sxs-lookup"><span data-stu-id="240a4-247">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="240a4-248">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="240a4-248">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="240a4-249">12</span><span class="sxs-lookup"><span data-stu-id="240a4-249">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="240a4-250">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-250">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="240a4-251">(13)</span><span class="sxs-lookup"><span data-stu-id="240a4-251">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="240a4-252">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="240a4-252">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="240a4-253">(14)</span><span class="sxs-lookup"><span data-stu-id="240a4-253">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="240a4-254">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="240a4-254">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="240a4-255">(15)</span><span class="sxs-lookup"><span data-stu-id="240a4-255">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="240a4-256">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="240a4-256">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="240a4-257">(16)</span><span class="sxs-lookup"><span data-stu-id="240a4-257">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="240a4-258">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="240a4-258">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="240a4-259">(17)</span><span class="sxs-lookup"><span data-stu-id="240a4-259">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="240a4-260">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-260">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="240a4-261">(18)</span><span class="sxs-lookup"><span data-stu-id="240a4-261">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="240a4-262">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="240a4-262">**Failure using the VxD loader.**</span></span> <span data-ttu-id="240a4-263">(19)</span><span class="sxs-lookup"><span data-stu-id="240a4-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="240a4-264">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="240a4-264">**Your registry might be corrupted.**</span></span> <span data-ttu-id="240a4-265">(20)</span><span class="sxs-lookup"><span data-stu-id="240a4-265">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="240a4-266">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-266">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="240a4-267">(21)</span><span class="sxs-lookup"><span data-stu-id="240a4-267">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="240a4-268">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="240a4-268">**This device is disabled.**</span></span> <span data-ttu-id="240a4-269">(22)</span><span class="sxs-lookup"><span data-stu-id="240a4-269">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="240a4-270">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="240a4-270">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="240a4-271">(23)</span><span class="sxs-lookup"><span data-stu-id="240a4-271">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="240a4-272">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="240a4-272">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="240a4-273">(24)</span><span class="sxs-lookup"><span data-stu-id="240a4-273">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="240a4-274">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-274">**Windows is still setting up this device.**</span></span> <span data-ttu-id="240a4-275">(25)</span><span class="sxs-lookup"><span data-stu-id="240a4-275">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="240a4-276">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-276">**Windows is still setting up this device.**</span></span> <span data-ttu-id="240a4-277">(26)</span><span class="sxs-lookup"><span data-stu-id="240a4-277">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="240a4-278">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="240a4-278">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="240a4-279">(27)</span><span class="sxs-lookup"><span data-stu-id="240a4-279">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="240a4-280">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="240a4-280">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="240a4-281">(28)</span><span class="sxs-lookup"><span data-stu-id="240a4-281">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="240a4-282">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="240a4-282">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="240a4-283">(29)</span><span class="sxs-lookup"><span data-stu-id="240a4-283">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="240a4-284">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="240a4-284">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="240a4-285">(30)</span><span class="sxs-lookup"><span data-stu-id="240a4-285">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="240a4-286">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="240a4-286">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="240a4-287">(31)</span><span class="sxs-lookup"><span data-stu-id="240a4-287">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="240a4-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-289">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="240a4-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-291">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="240a4-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-292">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="240a4-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="240a4-293">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="240a4-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-295">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-297">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="240a4-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="240a4-298">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="240a4-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="240a4-299">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="240a4-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="240a4-300">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-301">**Defaultblockize**</span><span class="sxs-lookup"><span data-stu-id="240a4-301">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-302">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a4-302">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-304">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="240a4-304">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-305">Tamanho de bloco padrão, em bytes, para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-305">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="240a4-306">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="240a4-306">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-307">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="240a4-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-310">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="240a4-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-311">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="240a4-311">A textual description of the object.</span></span>

<span data-ttu-id="240a4-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="240a4-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-316">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="240a4-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="240a4-317">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="240a4-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="240a4-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-320">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="240a4-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-322">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="240a4-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="240a4-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="240a4-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-327">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="240a4-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="240a4-328">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="240a4-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-332">Cadeia de caracteres de forma livre que descreve os tipos de detecção de erro e correção com suporte do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-332">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="240a4-333">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="240a4-333">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-334">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="240a4-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-335">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-336">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="240a4-336">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-337">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="240a4-337">Indicates when the object was installed.</span></span> <span data-ttu-id="240a4-338">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="240a4-338">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="240a4-339">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="240a4-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-341">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a4-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-342">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-343">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="240a4-344">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-345">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="240a4-345">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-346">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a4-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-348">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="240a4-348">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-349">Tamanho máximo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-349">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="240a4-350">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="240a4-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-351">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="240a4-351">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-352">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a4-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-354">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acesso sequencial DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="240a4-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-355">Tamanho máximo, em quilobytes, de mídia com suporte neste dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-355">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="240a4-356">Kilobytes são interpretados como o número de bytes multiplicado por 1000 (não o número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="240a4-356">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="240a4-357">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="240a4-357">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-358">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="240a4-358">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-359">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="240a4-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-361">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="240a4-361">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-362">Tamanho mínimo do bloco, em bytes, para a mídia acessada pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-362">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="240a4-363">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="240a4-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-364">**Nome**</span><span class="sxs-lookup"><span data-stu-id="240a4-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-367">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="240a4-367">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-368">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="240a4-368">Label by which the object is known.</span></span> <span data-ttu-id="240a4-369">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="240a4-369">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="240a4-370">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-371">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="240a4-371">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-372">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="240a4-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-374">Se **for true**, o dispositivo de acesso à mídia precisará de limpeza.</span><span class="sxs-lookup"><span data-stu-id="240a4-374">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="240a4-375">A limpeza manual ou automática é possível é indicada na propriedade da matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="240a4-375">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

</dd> <dt>

<span data-ttu-id="240a4-376">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="240a4-376">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-377">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="240a4-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-379">Número máximo de várias mídias individuais que podem ser suportadas ou inseridas.</span><span class="sxs-lookup"><span data-stu-id="240a4-379">Maximum number of multiple individual media that can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="240a4-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="240a4-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-383">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="240a4-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-384">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-384">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="240a4-385">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="240a4-385">Example: "\*PNP030b"</span></span>

<span data-ttu-id="240a4-386">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="240a4-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-388">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="240a4-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="240a4-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-390">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-390">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="240a4-391">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="240a4-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="240a4-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-393">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="240a4-393">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="240a4-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="240a4-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-395">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="240a4-395">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="240a4-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="240a4-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-397">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="240a4-397">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="240a4-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="240a4-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-399">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="240a4-399">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="240a4-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="240a4-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-401">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="240a4-401">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="240a4-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="240a4-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-403">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="240a4-403">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="240a4-404">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="240a4-404">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="240a4-405">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="240a4-405">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="240a4-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="240a4-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-407">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="240a4-407">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="240a4-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="240a4-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="240a4-409">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="240a4-409">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-410">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="240a4-410">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-411">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="240a4-411">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="240a4-413">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="240a4-413">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="240a4-414">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="240a4-414">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="240a4-415">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="240a4-415">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="240a4-416">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="240a4-416">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="240a4-417">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-418">**Status**</span><span class="sxs-lookup"><span data-stu-id="240a4-418">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-419">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-421">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="240a4-421">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-422">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="240a4-422">String that indicates the current status of the object.</span></span> <span data-ttu-id="240a4-423">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="240a4-423">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="240a4-424">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="240a4-424">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="240a4-425">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="240a4-425">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="240a4-426">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="240a4-426">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="240a4-427">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="240a4-427">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="240a4-428">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="240a4-428">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="240a4-429">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="240a4-430">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="240a4-430">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="240a4-431">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="240a4-431">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="240a4-432">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="240a4-432">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="240a4-433">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="240a4-433">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="240a4-434">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="240a4-434">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="240a4-435">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="240a4-435">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="240a4-436">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="240a4-436">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="240a4-437">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="240a4-437">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="240a4-438">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="240a4-438">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="240a4-439">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="240a4-439">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="240a4-440">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="240a4-440">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="240a4-441">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="240a4-441">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="240a4-442">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="240a4-442">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-443">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="240a4-443">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-444">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="240a4-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-445">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-446">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="240a4-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="240a4-447">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="240a4-447">State of the logical device.</span></span> <span data-ttu-id="240a4-448">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="240a4-448">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="240a4-449">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="240a4-450">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="240a4-450">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="240a4-451">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="240a4-451">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="240a4-452">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="240a4-452">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="240a4-453">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="240a4-453">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="240a4-454">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="240a4-454">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="240a4-455">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="240a4-455">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-456">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-458">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="240a4-458">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="240a4-459">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="240a4-459">The scoping system's creation class name.</span></span>

<span data-ttu-id="240a4-460">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="240a4-461">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="240a4-461">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="240a4-462">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="240a4-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="240a4-463">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="240a4-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="240a4-464">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="240a4-464">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="240a4-465">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="240a4-465">The scoping system's name.</span></span>

<span data-ttu-id="240a4-466">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-466">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="240a4-467">Comentários</span><span class="sxs-lookup"><span data-stu-id="240a4-467">Remarks</span></span>

<span data-ttu-id="240a4-468">A classe **CIM \_ MediaAccessDevice** é derivada do [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-468">The **CIM\_MediaAccessDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="240a4-469">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="240a4-469">WMI does not implement this class.</span></span> <span data-ttu-id="240a4-470">Para classes derivadas do **CIM \_ MediaAccessDevice**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="240a4-470">For classes derived from **CIM\_MediaAccessDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="240a4-471">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="240a4-471">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="240a4-472">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="240a4-472">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="240a4-473">Requisitos</span><span class="sxs-lookup"><span data-stu-id="240a4-473">Requirements</span></span>



| <span data-ttu-id="240a4-474">Requisito</span><span class="sxs-lookup"><span data-stu-id="240a4-474">Requirement</span></span> | <span data-ttu-id="240a4-475">Valor</span><span class="sxs-lookup"><span data-stu-id="240a4-475">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="240a4-476">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="240a4-476">Minimum supported client</span></span><br/> | <span data-ttu-id="240a4-477">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="240a4-477">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="240a4-478">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="240a4-478">Minimum supported server</span></span><br/> | <span data-ttu-id="240a4-479">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="240a4-479">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="240a4-480">Namespace</span><span class="sxs-lookup"><span data-stu-id="240a4-480">Namespace</span></span><br/>                | <span data-ttu-id="240a4-481">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="240a4-481">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="240a4-482">MOF</span><span class="sxs-lookup"><span data-stu-id="240a4-482">MOF</span></span><br/>                      | <dl> <span data-ttu-id="240a4-483"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="240a4-483"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="240a4-484">DLL</span><span class="sxs-lookup"><span data-stu-id="240a4-484">DLL</span></span><br/>                      | <dl> <span data-ttu-id="240a4-485"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="240a4-485"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="240a4-486">Confira também</span><span class="sxs-lookup"><span data-stu-id="240a4-486">See also</span></span>

<dl> <dt>

[<span data-ttu-id="240a4-487">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="240a4-487">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

