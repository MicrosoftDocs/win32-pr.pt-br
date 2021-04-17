---
description: A \_ classe CIM volumeset representa um intervalo contíguo de blocos lógicos apresentados ao ambiente operacional para leitura e gravação de dados do usuário.
ms.assetid: f0350185-6210-4f95-a2a2-23de61b1af1f
ms.tgt_platform: multiple
title: Classe CIM_VolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolumeSet
- CIM_VolumeSet.Access
- CIM_VolumeSet.Availability
- CIM_VolumeSet.BlockSize
- CIM_VolumeSet.Caption
- CIM_VolumeSet.ConfigManagerErrorCode
- CIM_VolumeSet.ConfigManagerUserConfig
- CIM_VolumeSet.CreationClassName
- CIM_VolumeSet.Description
- CIM_VolumeSet.DeviceID
- CIM_VolumeSet.ErrorCleared
- CIM_VolumeSet.ErrorDescription
- CIM_VolumeSet.ErrorMethodology
- CIM_VolumeSet.InstallDate
- CIM_VolumeSet.LastErrorCode
- CIM_VolumeSet.Name
- CIM_VolumeSet.NumberOfBlocks
- CIM_VolumeSet.PNPDeviceID
- CIM_VolumeSet.PowerManagementCapabilities
- CIM_VolumeSet.PowerManagementSupported
- CIM_VolumeSet.PSExtentInterleaveDepth
- CIM_VolumeSet.PSExtentStripeLength
- CIM_VolumeSet.Purpose
- CIM_VolumeSet.Status
- CIM_VolumeSet.StatusInfo
- CIM_VolumeSet.SystemCreationClassName
- CIM_VolumeSet.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ee8cd96381901250c9a15e544ee1963470565b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811163"
---
# <a name="cim_volumeset-class"></a><span data-ttu-id="12c07-103">Classe de volume do CIM \_</span><span class="sxs-lookup"><span data-stu-id="12c07-103">CIM\_VolumeSet class</span></span>

<span data-ttu-id="12c07-104">A classe **CIM \_ volumeset** representa um intervalo contíguo de blocos lógicos apresentados ao ambiente operacional para leitura e gravação de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="12c07-104">The **CIM\_VolumeSet** class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span> <span data-ttu-id="12c07-105">Os conjuntos de volumes não devem se sobrepor um ao outro e se baseiam em uma ou mais extensões físicas, extensões de espaço protegido ou extensões de agregação (todas do mesmo tipo).</span><span class="sxs-lookup"><span data-stu-id="12c07-105">Volume sets should not overlap one another and are based on one or more physical extents, protected space extents, or aggregate extents (all of the same type).</span></span> <span data-ttu-id="12c07-106">As associações com base em devem ser instanciadas ou subclasses conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="12c07-106">The based-on associations should be instantiated or subclassed as needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12c07-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="12c07-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="12c07-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="12c07-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="12c07-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="12c07-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="12c07-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="12c07-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c07-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12c07-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{35E25AA5-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VolumeSet : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   PSExtentInterleaveDepth;
  uint64   PSExtentStripeLength;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="12c07-112">Membros</span><span class="sxs-lookup"><span data-stu-id="12c07-112">Members</span></span>

<span data-ttu-id="12c07-113">A classe **CIM \_ volumeset** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12c07-113">The **CIM\_VolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="12c07-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="12c07-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="12c07-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12c07-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12c07-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="12c07-116">Methods</span></span>

<span data-ttu-id="12c07-117">A classe **CIM \_ volumeset** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="12c07-117">The **CIM\_VolumeSet** class has these methods.</span></span>



| <span data-ttu-id="12c07-118">Método</span><span class="sxs-lookup"><span data-stu-id="12c07-118">Method</span></span>                                                               | <span data-ttu-id="12c07-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="12c07-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12c07-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="12c07-120">**Reset**</span></span>](reset-method-in-class-cim-volumeset.md)                 | <span data-ttu-id="12c07-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12c07-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="12c07-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="12c07-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="12c07-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="12c07-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volumeset.md) | <span data-ttu-id="12c07-124">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="12c07-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="12c07-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="12c07-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="12c07-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12c07-126">Properties</span></span>

<span data-ttu-id="12c07-127">A classe **CIM \_ volumeset** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="12c07-127">The **CIM\_VolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12c07-128">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="12c07-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12c07-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-131">Propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="12c07-131">Read/write properties of the media.</span></span>

<span data-ttu-id="12c07-132">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12c07-133">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="12c07-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="12c07-134">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="12c07-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="12c07-135">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="12c07-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="12c07-136">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="12c07-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="12c07-137">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="12c07-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12c07-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="12c07-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12c07-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-141">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="12c07-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-142">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-142">Availability and status of the device.</span></span>

<span data-ttu-id="12c07-143">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12c07-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="12c07-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12c07-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="12c07-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="12c07-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="12c07-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="12c07-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="12c07-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="12c07-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="12c07-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12c07-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="12c07-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="12c07-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="12c07-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="12c07-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="12c07-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="12c07-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="12c07-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12c07-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="12c07-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="12c07-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="12c07-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="12c07-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="12c07-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="12c07-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="12c07-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-157">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="12c07-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="12c07-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="12c07-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-159">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="12c07-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="12c07-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="12c07-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-161">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="12c07-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="12c07-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="12c07-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="12c07-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-164">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="12c07-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="12c07-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="12c07-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-166">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="12c07-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="12c07-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="12c07-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-168">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="12c07-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="12c07-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="12c07-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-170">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="12c07-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="12c07-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="12c07-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-172">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="12c07-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12c07-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="12c07-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-174">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12c07-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-176">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="12c07-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-177">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12c07-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="12c07-178">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="12c07-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="12c07-179">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="12c07-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="12c07-180">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-180">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="12c07-181">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12c07-181">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-182">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="12c07-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-185">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="12c07-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-186">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="12c07-186">Short textual description of the object.</span></span>

<span data-ttu-id="12c07-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12c07-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-189">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12c07-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-191">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12c07-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-192">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="12c07-192">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="12c07-193">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="12c07-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="12c07-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="12c07-195"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="12c07-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-196">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="12c07-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="12c07-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="12c07-198">(1)</span><span class="sxs-lookup"><span data-stu-id="12c07-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-199">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12c07-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="12c07-201">(2)</span><span class="sxs-lookup"><span data-stu-id="12c07-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="12c07-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="12c07-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="12c07-203">(3)</span><span class="sxs-lookup"><span data-stu-id="12c07-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-204">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="12c07-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12c07-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="12c07-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="12c07-206">(4)</span><span class="sxs-lookup"><span data-stu-id="12c07-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-207">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-207">Device is not working properly.</span></span> <span data-ttu-id="12c07-208">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="12c07-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="12c07-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="12c07-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="12c07-210">(5)</span><span class="sxs-lookup"><span data-stu-id="12c07-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-211">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="12c07-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="12c07-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="12c07-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="12c07-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="12c07-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-214">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12c07-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="12c07-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="12c07-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="12c07-216">(7)</span><span class="sxs-lookup"><span data-stu-id="12c07-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="12c07-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="12c07-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="12c07-218">(8)</span><span class="sxs-lookup"><span data-stu-id="12c07-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-219">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="12c07-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="12c07-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="12c07-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="12c07-221">(9)</span><span class="sxs-lookup"><span data-stu-id="12c07-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-222">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-222">Device is not working properly.</span></span> <span data-ttu-id="12c07-223">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="12c07-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="12c07-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="12c07-225">(10)</span><span class="sxs-lookup"><span data-stu-id="12c07-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-226">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="12c07-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="12c07-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="12c07-228">(11)</span><span class="sxs-lookup"><span data-stu-id="12c07-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-229">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="12c07-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="12c07-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="12c07-231">12</span><span class="sxs-lookup"><span data-stu-id="12c07-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-232">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="12c07-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="12c07-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="12c07-234">(13)</span><span class="sxs-lookup"><span data-stu-id="12c07-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-235">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="12c07-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="12c07-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="12c07-237">(14)</span><span class="sxs-lookup"><span data-stu-id="12c07-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-238">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="12c07-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="12c07-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="12c07-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="12c07-240">(15)</span><span class="sxs-lookup"><span data-stu-id="12c07-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-241">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="12c07-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="12c07-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="12c07-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="12c07-243">(16)</span><span class="sxs-lookup"><span data-stu-id="12c07-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-244">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="12c07-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="12c07-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="12c07-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="12c07-246">(17)</span><span class="sxs-lookup"><span data-stu-id="12c07-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-247">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="12c07-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12c07-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="12c07-249">(18)</span><span class="sxs-lookup"><span data-stu-id="12c07-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-250">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="12c07-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="12c07-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="12c07-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="12c07-252">(19)</span><span class="sxs-lookup"><span data-stu-id="12c07-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="12c07-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="12c07-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="12c07-254">(20)</span><span class="sxs-lookup"><span data-stu-id="12c07-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-255">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="12c07-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="12c07-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="12c07-257">(21)</span><span class="sxs-lookup"><span data-stu-id="12c07-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-258">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="12c07-258">System failure.</span></span> <span data-ttu-id="12c07-259">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="12c07-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="12c07-260">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="12c07-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="12c07-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="12c07-262">(22)</span><span class="sxs-lookup"><span data-stu-id="12c07-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-263">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="12c07-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="12c07-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="12c07-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="12c07-265">(23)</span><span class="sxs-lookup"><span data-stu-id="12c07-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-266">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="12c07-266">System failure.</span></span> <span data-ttu-id="12c07-267">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="12c07-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="12c07-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="12c07-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="12c07-269">(24)</span><span class="sxs-lookup"><span data-stu-id="12c07-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-270">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="12c07-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12c07-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12c07-272">(25)</span><span class="sxs-lookup"><span data-stu-id="12c07-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-273">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="12c07-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="12c07-275">(26)</span><span class="sxs-lookup"><span data-stu-id="12c07-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-276">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="12c07-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="12c07-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="12c07-278">(27)</span><span class="sxs-lookup"><span data-stu-id="12c07-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-279">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="12c07-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="12c07-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="12c07-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="12c07-281">(28)</span><span class="sxs-lookup"><span data-stu-id="12c07-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-282">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="12c07-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="12c07-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="12c07-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="12c07-284">(29)</span><span class="sxs-lookup"><span data-stu-id="12c07-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-285">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="12c07-285">Device is disabled.</span></span> <span data-ttu-id="12c07-286">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="12c07-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="12c07-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="12c07-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="12c07-288">(30)</span><span class="sxs-lookup"><span data-stu-id="12c07-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-289">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="12c07-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="12c07-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="12c07-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="12c07-291">(31)</span><span class="sxs-lookup"><span data-stu-id="12c07-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-292">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-292">Device is not working properly.</span></span> <span data-ttu-id="12c07-293">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="12c07-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12c07-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="12c07-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-295">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12c07-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-297">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12c07-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-298">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="12c07-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="12c07-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12c07-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-303">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12c07-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12c07-304">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="12c07-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="12c07-305">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="12c07-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="12c07-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-307">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12c07-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-310">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="12c07-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-311">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="12c07-311">Textual description of the object.</span></span>

<span data-ttu-id="12c07-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="12c07-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-316">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12c07-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12c07-317">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12c07-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="12c07-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="12c07-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-320">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12c07-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-322">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="12c07-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="12c07-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="12c07-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-327">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="12c07-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="12c07-328">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="12c07-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-332">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12c07-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="12c07-333">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="12c07-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-335">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="12c07-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="12c07-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-338">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="12c07-338">Date and time the object was installed.</span></span> <span data-ttu-id="12c07-339">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="12c07-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="12c07-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="12c07-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-342">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12c07-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-344">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12c07-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="12c07-345">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-346">**Nome**</span><span class="sxs-lookup"><span data-stu-id="12c07-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-349">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="12c07-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-350">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="12c07-350">Label by which the object is known.</span></span> <span data-ttu-id="12c07-351">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="12c07-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="12c07-352">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="12c07-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-354">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12c07-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-356">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="12c07-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-357">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12c07-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="12c07-358">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="12c07-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="12c07-359">Se o valor de **BlockSize** for 1 (um), essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="12c07-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="12c07-360">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="12c07-361">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12c07-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="12c07-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-365">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="12c07-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-366">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12c07-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="12c07-367">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="12c07-368">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="12c07-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="12c07-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="12c07-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12c07-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="12c07-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-372">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12c07-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="12c07-373">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="12c07-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12c07-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="12c07-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="12c07-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="12c07-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12c07-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="12c07-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12c07-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="12c07-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-378">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="12c07-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="12c07-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="12c07-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-380">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="12c07-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="12c07-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="12c07-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-382">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="12c07-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="12c07-383">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="12c07-383">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="12c07-384">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="12c07-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="12c07-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="12c07-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-386">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="12c07-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="12c07-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="12c07-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="12c07-388">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="12c07-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12c07-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="12c07-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-390">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="12c07-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-392">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="12c07-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="12c07-393">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="12c07-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="12c07-394">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="12c07-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="12c07-395">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="12c07-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="12c07-396">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-397">**PSExtentInterleaveDepth**</span><span class="sxs-lookup"><span data-stu-id="12c07-397">**PSExtentInterleaveDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-398">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12c07-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-400">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Conjunto de volumes DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="12c07-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-401">Número de extensões de espaço protegido para distribuição como um conjunto coletivo.</span><span class="sxs-lookup"><span data-stu-id="12c07-401">Number of protected space extents to stripe as a collective set.</span></span> <span data-ttu-id="12c07-402">No SCC, esse valor é definido como o número de faixas a serem contadas antes de continuar a mapear para o próximo conjunto contíguo de extensões, além da faixa atual.</span><span class="sxs-lookup"><span data-stu-id="12c07-402">In SCC, this value is defined as the number of stripes to count before continuing to map into the next contiguous set of extents, beyond the current stripe.</span></span>

<span data-ttu-id="12c07-403">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12c07-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-404">**PSExtentStripeLength**</span><span class="sxs-lookup"><span data-stu-id="12c07-404">**PSExtentStripeLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-405">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="12c07-405">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-406">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-407">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Conjunto de volumes DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="12c07-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-408">Número de extensões de espaço protegido contíguos contadas antes do loop voltar à primeira extensão de espaço protegido da faixa atual.</span><span class="sxs-lookup"><span data-stu-id="12c07-408">Number of contiguous protected space extents counted before looping back to the first protected space extent of the current stripe.</span></span> <span data-ttu-id="12c07-409">É o número de extensões que formam a faixa de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="12c07-409">It is the number of extents forming the user data stripe.</span></span>

<span data-ttu-id="12c07-410">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="12c07-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-411">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="12c07-411">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12c07-414">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="12c07-414">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="12c07-415">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-415">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-416">**Status**</span><span class="sxs-lookup"><span data-stu-id="12c07-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-417">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-418">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-419">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="12c07-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-420">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="12c07-420">Current status of the object.</span></span> <span data-ttu-id="12c07-421">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="12c07-422">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="12c07-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="12c07-423">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="12c07-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="12c07-424">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="12c07-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="12c07-425">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="12c07-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12c07-426">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="12c07-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="12c07-427">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="12c07-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="12c07-428">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="12c07-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="12c07-429">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="12c07-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="12c07-430">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="12c07-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="12c07-431">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="12c07-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="12c07-432">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="12c07-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="12c07-433">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="12c07-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="12c07-434">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="12c07-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12c07-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="12c07-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-436">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12c07-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-438">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="12c07-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="12c07-439">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="12c07-439">State of the logical device.</span></span> <span data-ttu-id="12c07-440">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="12c07-440">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="12c07-441">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12c07-442">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="12c07-442">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12c07-443">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="12c07-443">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="12c07-444">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="12c07-444">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="12c07-445">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="12c07-445">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="12c07-446">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="12c07-446">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12c07-447">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="12c07-447">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-448">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-449">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-450">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12c07-450">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12c07-451">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="12c07-451">Scoping system's creation class name.</span></span>

<span data-ttu-id="12c07-452">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c07-453">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="12c07-453">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12c07-454">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="12c07-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12c07-455">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12c07-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12c07-456">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12c07-456">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12c07-457">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="12c07-457">Scoping system's name.</span></span>

<span data-ttu-id="12c07-458">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12c07-459">Comentários</span><span class="sxs-lookup"><span data-stu-id="12c07-459">Remarks</span></span>

<span data-ttu-id="12c07-460">A classe **CIM \_ volumeset** é derivada de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="12c07-460">The **CIM\_VolumeSet** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="12c07-461">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="12c07-461">WMI does not implement this class.</span></span>

<span data-ttu-id="12c07-462">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="12c07-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="12c07-463">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="12c07-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c07-464">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12c07-464">Requirements</span></span>



| <span data-ttu-id="12c07-465">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c07-465">Requirement</span></span> | <span data-ttu-id="12c07-466">Valor</span><span class="sxs-lookup"><span data-stu-id="12c07-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12c07-467">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c07-467">Minimum supported client</span></span><br/> | <span data-ttu-id="12c07-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12c07-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12c07-469">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c07-469">Minimum supported server</span></span><br/> | <span data-ttu-id="12c07-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12c07-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12c07-471">Namespace</span><span class="sxs-lookup"><span data-stu-id="12c07-471">Namespace</span></span><br/>                | <span data-ttu-id="12c07-472">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12c07-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12c07-473">MOF</span><span class="sxs-lookup"><span data-stu-id="12c07-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12c07-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12c07-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12c07-475">DLL</span><span class="sxs-lookup"><span data-stu-id="12c07-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12c07-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c07-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c07-477">Confira também</span><span class="sxs-lookup"><span data-stu-id="12c07-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c07-478">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="12c07-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

