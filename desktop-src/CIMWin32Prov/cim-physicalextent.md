---
description: A \_ classe CIM PhysicalExtent representa uma implementação de RAID SCC.
ms.assetid: d1950464-e17a-4651-aa53-6385659994ff
ms.tgt_platform: multiple
title: Classe CIM_PhysicalExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent
- CIM_PhysicalExtent.Access
- CIM_PhysicalExtent.Availability
- CIM_PhysicalExtent.BlockSize
- CIM_PhysicalExtent.Caption
- CIM_PhysicalExtent.ConfigManagerErrorCode
- CIM_PhysicalExtent.ConfigManagerUserConfig
- CIM_PhysicalExtent.CreationClassName
- CIM_PhysicalExtent.Description
- CIM_PhysicalExtent.DeviceID
- CIM_PhysicalExtent.ErrorCleared
- CIM_PhysicalExtent.ErrorDescription
- CIM_PhysicalExtent.ErrorMethodology
- CIM_PhysicalExtent.InstallDate
- CIM_PhysicalExtent.LastErrorCode
- CIM_PhysicalExtent.Name
- CIM_PhysicalExtent.NumberOfBlocks
- CIM_PhysicalExtent.PNPDeviceID
- CIM_PhysicalExtent.PowerManagementCapabilities
- CIM_PhysicalExtent.PowerManagementSupported
- CIM_PhysicalExtent.Purpose
- CIM_PhysicalExtent.Status
- CIM_PhysicalExtent.StatusInfo
- CIM_PhysicalExtent.SystemCreationClassName
- CIM_PhysicalExtent.SystemName
- CIM_PhysicalExtent.UnitsBeforeCheckDataInterleave
- CIM_PhysicalExtent.UnitsOfCheckData
- CIM_PhysicalExtent.UnitsOfUserData
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 31e05d3b339d64fd640460716376c3d8b538fa95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646236"
---
# <a name="cim_physicalextent-class"></a><span data-ttu-id="5d4ab-103">\_Classe CIM PhysicalExtent</span><span class="sxs-lookup"><span data-stu-id="5d4ab-103">CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="5d4ab-104">A classe **CIM \_ PhysicalExtent** representa uma implementação de RAID SCC.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-104">The **CIM\_PhysicalExtent** class represents an SCC RAID implementation.</span></span> <span data-ttu-id="5d4ab-105">Ele define os endereços de bloco endereçáveis consecutivos em um único dispositivo de armazenamento que são tratados como uma única extensão de armazenamento na mesma classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="5d4ab-105">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="5d4ab-106">Uma alternativa, quando a configuração automática é usada, é instanciar ou estender a classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="5d4ab-106">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d4ab-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5d4ab-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5d4ab-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5d4ab-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4ab-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d4ab-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979E-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalExtent : CIM_StorageExtent
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
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   UnitsBeforeCheckDataInterleave;
  uint64   UnitsOfCheckData;
  uint64   UnitsOfUserData;
};
```

## <a name="members"></a><span data-ttu-id="5d4ab-112">Membros</span><span class="sxs-lookup"><span data-stu-id="5d4ab-112">Members</span></span>

<span data-ttu-id="5d4ab-113">A classe **CIM \_ PhysicalExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d4ab-113">The **CIM\_PhysicalExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="5d4ab-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d4ab-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5d4ab-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d4ab-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5d4ab-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5d4ab-116">Methods</span></span>

<span data-ttu-id="5d4ab-117">A classe **CIM \_ PhysicalExtent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-117">The **CIM\_PhysicalExtent** class has these methods.</span></span>



| <span data-ttu-id="5d4ab-118">Método</span><span class="sxs-lookup"><span data-stu-id="5d4ab-118">Method</span></span>                                                                    | <span data-ttu-id="5d4ab-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d4ab-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d4ab-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-120">**Reset**</span></span>](reset-method-in-class-cim-physicalextent.md)                 | <span data-ttu-id="5d4ab-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="5d4ab-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="5d4ab-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-physicalextent.md) | <span data-ttu-id="5d4ab-124">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="5d4ab-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5d4ab-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d4ab-126">Properties</span></span>

<span data-ttu-id="5d4ab-127">A classe **CIM \_ PhysicalExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-127">The **CIM\_PhysicalExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d4ab-128">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-131">Propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-131">Read/write properties of the media.</span></span>

<span data-ttu-id="5d4ab-132">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d4ab-133">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="5d4ab-134">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="5d4ab-135">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="5d4ab-136">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="5d4ab-137">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d4ab-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-141">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-142">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-142">Availability and status of the device.</span></span>

<span data-ttu-id="5d4ab-143">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d4ab-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d4ab-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5d4ab-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-147">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="5d4ab-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5d4ab-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5d4ab-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5d4ab-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5d4ab-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="5d4ab-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5d4ab-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5d4ab-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5d4ab-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5d4ab-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5d4ab-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5d4ab-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-158">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5d4ab-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-160">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5d4ab-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-162">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5d4ab-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5d4ab-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-165">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5d4ab-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-167">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5d4ab-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-169">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5d4ab-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-171">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5d4ab-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-173">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d4ab-174">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-174">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-175">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-177">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensão física de DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-177">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-178">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-178">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="5d4ab-179">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-179">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="5d4ab-180">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-180">If the block size is unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one) .</span></span>

<span data-ttu-id="5d4ab-181">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5d4ab-182">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-183">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-186">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-187">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-187">Short textual description of the object.</span></span>

<span data-ttu-id="5d4ab-188">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-190">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-192">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-193">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="5d4ab-194">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5d4ab-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5d4ab-196"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-197">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5d4ab-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5d4ab-199">(1)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-200">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5d4ab-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5d4ab-202">(2)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5d4ab-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5d4ab-204">(3)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-205">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5d4ab-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5d4ab-207">(4)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-208">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-208">Device is not working properly.</span></span> <span data-ttu-id="5d4ab-209">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5d4ab-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5d4ab-211">(5)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-212">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5d4ab-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5d4ab-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-215">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5d4ab-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5d4ab-217">(7)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5d4ab-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5d4ab-219">(8)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-220">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5d4ab-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5d4ab-222">(9)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-223">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-223">Device is not working properly.</span></span> <span data-ttu-id="5d4ab-224">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5d4ab-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5d4ab-226">(10)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-227">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5d4ab-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5d4ab-229">(11)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-230">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5d4ab-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5d4ab-232">12</span><span class="sxs-lookup"><span data-stu-id="5d4ab-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-233">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5d4ab-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5d4ab-235">(13)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-236">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5d4ab-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5d4ab-238">(14)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-239">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5d4ab-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5d4ab-241">(15)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-242">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5d4ab-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5d4ab-244">(16)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-245">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5d4ab-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5d4ab-247">(17)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-248">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5d4ab-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5d4ab-250">(18)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-251">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5d4ab-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5d4ab-253">(19)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5d4ab-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5d4ab-255">(20)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-256">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5d4ab-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5d4ab-258">(21)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-259">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-259">System failure.</span></span> <span data-ttu-id="5d4ab-260">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5d4ab-261">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5d4ab-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5d4ab-263">(22)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-264">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5d4ab-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5d4ab-266">(23)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-267">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-267">System failure.</span></span> <span data-ttu-id="5d4ab-268">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5d4ab-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5d4ab-270">(24)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-271">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5d4ab-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5d4ab-273">(25)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-274">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5d4ab-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5d4ab-276">(26)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-277">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5d4ab-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5d4ab-279">(27)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-280">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5d4ab-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5d4ab-282">(28)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-283">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5d4ab-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5d4ab-285">(29)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-286">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-286">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5d4ab-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5d4ab-288">(30)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-289">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5d4ab-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5d4ab-291">(31)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-292">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-292">Device is not working properly.</span></span> <span data-ttu-id="5d4ab-293">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d4ab-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-295">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-296">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-297">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-298">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5d4ab-299">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-301">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-303">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-304">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5d4ab-305">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5d4ab-306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-307">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-308">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-310">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-311">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-311">Textual description of the object.</span></span>

<span data-ttu-id="5d4ab-312">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-314">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-315">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-316">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-317">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5d4ab-318">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-320">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-322">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5d4ab-323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-325">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-327">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5d4ab-328">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-332">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="5d4ab-333">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-335">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-337">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-338">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-338">Date and time the object was installed.</span></span> <span data-ttu-id="5d4ab-339">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5d4ab-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-342">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-344">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5d4ab-345">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-346">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-347">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-348">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-349">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-350">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-350">Label by which the object is known.</span></span> <span data-ttu-id="5d4ab-351">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5d4ab-352">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-354">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-356">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensão física de DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-356">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-357">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="5d4ab-358">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="5d4ab-359">Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="5d4ab-360">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5d4ab-361">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-363">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-364">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-365">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-366">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="5d4ab-367">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5d4ab-368">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5d4ab-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-370">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-371">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-372">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5d4ab-373">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d4ab-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5d4ab-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5d4ab-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5d4ab-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-378">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5d4ab-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-380">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5d4ab-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-382">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5d4ab-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5d4ab-383">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5d4ab-384">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5d4ab-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-386">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5d4ab-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5d4ab-388">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5d4ab-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-390">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-391">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-392">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5d4ab-393">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5d4ab-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5d4ab-394">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5d4ab-395">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5d4ab-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="5d4ab-396">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-397">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-398">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-399">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-400">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-400">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="5d4ab-401">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-402">**Status**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-402">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-405">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-406">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-406">Current status of the object.</span></span>

<span data-ttu-id="5d4ab-407">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5d4ab-408">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5d4ab-408">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5d4ab-409">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-409">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5d4ab-410">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-410">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5d4ab-411">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-411">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d4ab-412">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-412">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5d4ab-413">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-413">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5d4ab-414">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-414">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5d4ab-415">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-415">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5d4ab-416">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-416">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5d4ab-417">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-417">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5d4ab-418">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-418">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5d4ab-419">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-419">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5d4ab-420">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-420">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d4ab-421">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-421">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-422">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-423">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-424">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-425">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-425">State of the logical device.</span></span> <span data-ttu-id="5d4ab-426">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-426">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5d4ab-427">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5d4ab-428">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-428">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d4ab-429">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-429">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5d4ab-430">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5d4ab-431">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-431">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5d4ab-432">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-432">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d4ab-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-436">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-437">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-437">Scoping system's creation class name.</span></span>

<span data-ttu-id="5d4ab-438">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-442">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5d4ab-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-443">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-443">Scoping system's name.</span></span>

<span data-ttu-id="5d4ab-444">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-445">**UnitsBeforeCheckDataInterleave**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-445">**UnitsBeforeCheckDataInterleave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-446">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-446">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-447">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-448">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensão física de DMTF \| 1,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-449">Número de bytes de dados de usuário a serem ignorados antes de iniciar a intercalação de dados de verificação.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-449">Number of user data bytes to skip before starting the check-data interleave.</span></span>

<span data-ttu-id="5d4ab-450">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-451">**UnitsOfCheckData**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-451">**UnitsOfCheckData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-452">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-452">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-454">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensão física de DMTF \| 1,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-455">Número de bytes a serem reservados para dados de verificação.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-455">Number of bytes to be reserved for check data.</span></span>

<span data-ttu-id="5d4ab-456">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-456">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5d4ab-457">**UnitsOfUserData**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-457">**UnitsOfUserData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d4ab-458">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-458">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d4ab-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d4ab-460">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensão física de DMTF \| 1,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5d4ab-460">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5d4ab-461">Número de bytes a serem reservados para dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-461">Number of bytes to be reserved for user data.</span></span>

<span data-ttu-id="5d4ab-462">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-462">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d4ab-463">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d4ab-463">Remarks</span></span>

<span data-ttu-id="5d4ab-464">A classe **CIM \_ PhysicalExtent** é derivada de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5d4ab-464">The **CIM\_PhysicalExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5d4ab-465">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-465">WMI does not implement this class.</span></span>

<span data-ttu-id="5d4ab-466">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-466">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5d4ab-467">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5d4ab-467">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4ab-468">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d4ab-468">Requirements</span></span>



| <span data-ttu-id="5d4ab-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d4ab-469">Requirement</span></span> | <span data-ttu-id="5d4ab-470">Valor</span><span class="sxs-lookup"><span data-stu-id="5d4ab-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4ab-471">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d4ab-471">Minimum supported client</span></span><br/> | <span data-ttu-id="5d4ab-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d4ab-472">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d4ab-473">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d4ab-473">Minimum supported server</span></span><br/> | <span data-ttu-id="5d4ab-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d4ab-474">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d4ab-475">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d4ab-475">Namespace</span></span><br/>                | <span data-ttu-id="5d4ab-476">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5d4ab-476">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d4ab-477">MOF</span><span class="sxs-lookup"><span data-stu-id="5d4ab-477">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d4ab-478"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d4ab-478"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d4ab-479">DLL</span><span class="sxs-lookup"><span data-stu-id="5d4ab-479">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d4ab-480"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d4ab-480"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d4ab-481">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d4ab-481">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4ab-482">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5d4ab-482">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

