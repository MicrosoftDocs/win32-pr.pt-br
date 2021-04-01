---
description: A \_ classe CIM AggregatePSExtent define o número de blocos lógicos endereçáveis em um único dispositivo de armazenamento, excluindo blocos lógicos mapeados como dados de verificação.
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: Classe CIM_AggregatePSExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646454"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="6c63f-103">\_Classe CIM AggregatePSExtent</span><span class="sxs-lookup"><span data-stu-id="6c63f-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="6c63f-104">A classe **CIM \_ AggregatePSExtent** define o número de blocos lógicos endereçáveis em um único dispositivo de armazenamento, excluindo blocos lógicos mapeados como dados de verificação.</span><span class="sxs-lookup"><span data-stu-id="6c63f-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="6c63f-105">Se os conjuntos de volumes forem definidos, os blocos lógicos estarão contidos em um único conjunto de volumes.</span><span class="sxs-lookup"><span data-stu-id="6c63f-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="6c63f-106">Esse é um agrupamento alternativo para [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md), quando apenas informações resumidas são necessárias ou quando a configuração automática é usada.</span><span class="sxs-lookup"><span data-stu-id="6c63f-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="6c63f-107">A configuração automática pode resultar em milhares de classes de [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md) sendo definidas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="6c63f-108">A classe **CIM \_ AggregatePSExtent** foi definida para que extensões individuais não precisem ser modeladas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c63f-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6c63f-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6c63f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6c63f-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6c63f-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6c63f-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c63f-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c63f-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
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
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="6c63f-114">Membros</span><span class="sxs-lookup"><span data-stu-id="6c63f-114">Members</span></span>

<span data-ttu-id="6c63f-115">A classe **CIM \_ AggregatePSExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6c63f-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="6c63f-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c63f-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c63f-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c63f-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c63f-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c63f-118">Methods</span></span>

<span data-ttu-id="6c63f-119">A classe **CIM \_ AggregatePSExtent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6c63f-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="6c63f-120">Método</span><span class="sxs-lookup"><span data-stu-id="6c63f-120">Method</span></span>                                                                       | <span data-ttu-id="6c63f-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c63f-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c63f-122">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="6c63f-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="6c63f-123">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6c63f-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="6c63f-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6c63f-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="6c63f-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6c63f-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="6c63f-126">Define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="6c63f-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="6c63f-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6c63f-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c63f-128">Properties</span></span>

<span data-ttu-id="6c63f-129">A classe **CIM \_ AggregatePSExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6c63f-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c63f-130">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="6c63f-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c63f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-133">Descreve as propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="6c63f-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="6c63f-134">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c63f-135">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6c63f-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="6c63f-136">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="6c63f-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="6c63f-137">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="6c63f-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="6c63f-138">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="6c63f-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="6c63f-139">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="6c63f-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c63f-140">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="6c63f-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c63f-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6c63f-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-144">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c63f-144">Availability and status of the device.</span></span>

<span data-ttu-id="6c63f-145">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c63f-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6c63f-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c63f-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="6c63f-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6c63f-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="6c63f-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6c63f-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="6c63f-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6c63f-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="6c63f-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6c63f-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="6c63f-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6c63f-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="6c63f-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6c63f-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="6c63f-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6c63f-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="6c63f-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6c63f-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="6c63f-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6c63f-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="6c63f-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6c63f-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="6c63f-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6c63f-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="6c63f-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-159">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6c63f-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6c63f-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="6c63f-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-161">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6c63f-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="6c63f-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-163">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="6c63f-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6c63f-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="6c63f-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6c63f-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="6c63f-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-166">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="6c63f-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6c63f-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="6c63f-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-168">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="6c63f-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6c63f-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="6c63f-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-170">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="6c63f-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6c63f-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="6c63f-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-172">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6c63f-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="6c63f-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-174">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="6c63f-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c63f-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="6c63f-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-176">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c63f-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-178">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="6c63f-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-179">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c63f-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="6c63f-180">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="6c63f-181">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="6c63f-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="6c63f-182">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6c63f-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6c63f-183">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6c63f-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-187">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6c63f-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-188">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6c63f-188">A short textual description of the object.</span></span>

<span data-ttu-id="6c63f-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6c63f-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-191">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c63f-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-193">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6c63f-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-194">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6c63f-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6c63f-195">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6c63f-196">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-196">**This device is working properly.**</span></span> <span data-ttu-id="6c63f-197"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="6c63f-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6c63f-198">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="6c63f-199">(1)</span><span class="sxs-lookup"><span data-stu-id="6c63f-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6c63f-200">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6c63f-201">(2)</span><span class="sxs-lookup"><span data-stu-id="6c63f-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6c63f-202">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6c63f-203">(3)</span><span class="sxs-lookup"><span data-stu-id="6c63f-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6c63f-204">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6c63f-205">(4)</span><span class="sxs-lookup"><span data-stu-id="6c63f-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6c63f-206">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6c63f-207">(5)</span><span class="sxs-lookup"><span data-stu-id="6c63f-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6c63f-208">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6c63f-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="6c63f-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6c63f-210">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-210">**Cannot filter.**</span></span> <span data-ttu-id="6c63f-211">(7)</span><span class="sxs-lookup"><span data-stu-id="6c63f-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6c63f-212">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6c63f-213">(8)</span><span class="sxs-lookup"><span data-stu-id="6c63f-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6c63f-214">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6c63f-215">(9)</span><span class="sxs-lookup"><span data-stu-id="6c63f-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6c63f-216">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-216">**This device cannot start.**</span></span> <span data-ttu-id="6c63f-217">(10)</span><span class="sxs-lookup"><span data-stu-id="6c63f-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6c63f-218">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-218">**This device failed.**</span></span> <span data-ttu-id="6c63f-219">(11)</span><span class="sxs-lookup"><span data-stu-id="6c63f-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6c63f-220">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6c63f-221">12</span><span class="sxs-lookup"><span data-stu-id="6c63f-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6c63f-222">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6c63f-223">(13)</span><span class="sxs-lookup"><span data-stu-id="6c63f-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6c63f-224">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6c63f-225">(14)</span><span class="sxs-lookup"><span data-stu-id="6c63f-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6c63f-226">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6c63f-227">(15)</span><span class="sxs-lookup"><span data-stu-id="6c63f-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6c63f-228">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6c63f-229">(16)</span><span class="sxs-lookup"><span data-stu-id="6c63f-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6c63f-230">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6c63f-231">(17)</span><span class="sxs-lookup"><span data-stu-id="6c63f-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6c63f-232">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6c63f-233">(18)</span><span class="sxs-lookup"><span data-stu-id="6c63f-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6c63f-234">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="6c63f-235">(19)</span><span class="sxs-lookup"><span data-stu-id="6c63f-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6c63f-236">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="6c63f-237">(20)</span><span class="sxs-lookup"><span data-stu-id="6c63f-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6c63f-238">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6c63f-239">(21)</span><span class="sxs-lookup"><span data-stu-id="6c63f-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6c63f-240">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-240">**This device is disabled.**</span></span> <span data-ttu-id="6c63f-241">(22)</span><span class="sxs-lookup"><span data-stu-id="6c63f-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6c63f-242">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6c63f-243">(23)</span><span class="sxs-lookup"><span data-stu-id="6c63f-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6c63f-244">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6c63f-245">(24)</span><span class="sxs-lookup"><span data-stu-id="6c63f-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6c63f-246">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="6c63f-247">(25)</span><span class="sxs-lookup"><span data-stu-id="6c63f-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6c63f-248">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="6c63f-249">(26)</span><span class="sxs-lookup"><span data-stu-id="6c63f-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6c63f-250">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6c63f-251">(27)</span><span class="sxs-lookup"><span data-stu-id="6c63f-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6c63f-252">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6c63f-253">(28)</span><span class="sxs-lookup"><span data-stu-id="6c63f-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6c63f-254">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6c63f-255">(29)</span><span class="sxs-lookup"><span data-stu-id="6c63f-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6c63f-256">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6c63f-257">(30)</span><span class="sxs-lookup"><span data-stu-id="6c63f-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6c63f-258">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6c63f-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6c63f-259">(31)</span><span class="sxs-lookup"><span data-stu-id="6c63f-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c63f-260">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6c63f-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-261">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6c63f-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-263">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6c63f-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-264">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6c63f-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6c63f-265">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-266">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6c63f-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-267">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-268">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-269">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c63f-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-270">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="6c63f-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6c63f-271">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="6c63f-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6c63f-272">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-273">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6c63f-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-274">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-276">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="6c63f-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-277">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6c63f-277">A textual description of the object.</span></span>

<span data-ttu-id="6c63f-278">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-279">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6c63f-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-280">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-282">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c63f-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-283">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6c63f-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6c63f-284">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-285">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6c63f-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-286">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6c63f-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-288">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="6c63f-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6c63f-289">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6c63f-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-291">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-292">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-293">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6c63f-294">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-295">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="6c63f-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-298">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c63f-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="6c63f-299">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6c63f-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-301">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6c63f-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-303">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="6c63f-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-304">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-304">Indicates when the object was installed.</span></span> <span data-ttu-id="6c63f-305">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6c63f-306">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-307">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6c63f-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-308">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c63f-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-310">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6c63f-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6c63f-311">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-312">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6c63f-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-315">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6c63f-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-316">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="6c63f-316">Label by which the object is known.</span></span> <span data-ttu-id="6c63f-317">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="6c63f-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6c63f-318">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="6c63f-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-320">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c63f-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-322">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="6c63f-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-323">Número de blocos consecutivos, cada um deles bloqueia o tamanho do valor contido na propriedade **BlockSize** , que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c63f-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="6c63f-324">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6c63f-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="6c63f-325">Se o valor de **BlockSize** for 1 (um), essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c63f-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="6c63f-326">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6c63f-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6c63f-327">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6c63f-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-331">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6c63f-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-332">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6c63f-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6c63f-333">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6c63f-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="6c63f-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6c63f-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-336">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c63f-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-338">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6c63f-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="6c63f-339">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c63f-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6c63f-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-341">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6c63f-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="6c63f-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-343">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6c63f-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6c63f-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="6c63f-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-345">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="6c63f-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6c63f-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6c63f-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-347">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6c63f-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6c63f-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="6c63f-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-349">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="6c63f-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6c63f-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="6c63f-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-351">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="6c63f-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="6c63f-352">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="6c63f-353">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6c63f-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6c63f-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="6c63f-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-355">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="6c63f-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6c63f-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="6c63f-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6c63f-357">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="6c63f-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6c63f-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6c63f-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-359">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6c63f-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-360">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-361">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="6c63f-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6c63f-362">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6c63f-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6c63f-363">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="6c63f-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6c63f-364">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6c63f-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6c63f-365">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-366">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="6c63f-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-369">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="6c63f-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="6c63f-370">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-371">**Status**</span><span class="sxs-lookup"><span data-stu-id="6c63f-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-372">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-374">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6c63f-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-375">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6c63f-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="6c63f-376">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="6c63f-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6c63f-377">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="6c63f-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6c63f-378">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="6c63f-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6c63f-379">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6c63f-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6c63f-380">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6c63f-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6c63f-381">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6c63f-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6c63f-382">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6c63f-383">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6c63f-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6c63f-384">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6c63f-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6c63f-385">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="6c63f-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6c63f-386">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6c63f-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c63f-387">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6c63f-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6c63f-388">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6c63f-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6c63f-389">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6c63f-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6c63f-390">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="6c63f-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6c63f-391">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="6c63f-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6c63f-392">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="6c63f-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6c63f-393">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6c63f-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6c63f-394">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="6c63f-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6c63f-395">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="6c63f-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c63f-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6c63f-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-397">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c63f-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-399">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="6c63f-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-400">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6c63f-400">State of the logical device.</span></span> <span data-ttu-id="6c63f-401">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="6c63f-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="6c63f-402">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6c63f-403">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6c63f-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6c63f-404">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="6c63f-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6c63f-405">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6c63f-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6c63f-406">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="6c63f-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6c63f-407">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="6c63f-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c63f-408">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6c63f-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-409">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-411">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c63f-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-412">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="6c63f-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="6c63f-413">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c63f-414">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6c63f-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c63f-415">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6c63f-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-416">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c63f-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c63f-417">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c63f-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c63f-418">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="6c63f-418">The scoping system's name.</span></span>

<span data-ttu-id="6c63f-419">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c63f-420">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c63f-420">Remarks</span></span>

<span data-ttu-id="6c63f-421">A classe **CIM \_ AggregatePSExtent** é derivada de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="6c63f-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="6c63f-422">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="6c63f-422">WMI does not implement this class.</span></span>

<span data-ttu-id="6c63f-423">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="6c63f-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6c63f-424">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="6c63f-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c63f-425">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c63f-425">Requirements</span></span>



| <span data-ttu-id="6c63f-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c63f-426">Requirement</span></span> | <span data-ttu-id="6c63f-427">Valor</span><span class="sxs-lookup"><span data-stu-id="6c63f-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c63f-428">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c63f-428">Minimum supported client</span></span><br/> | <span data-ttu-id="6c63f-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c63f-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c63f-430">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c63f-430">Minimum supported server</span></span><br/> | <span data-ttu-id="6c63f-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c63f-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c63f-432">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c63f-432">Namespace</span></span><br/>                | <span data-ttu-id="6c63f-433">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6c63f-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c63f-434">MOF</span><span class="sxs-lookup"><span data-stu-id="6c63f-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c63f-435"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c63f-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c63f-436">DLL</span><span class="sxs-lookup"><span data-stu-id="6c63f-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c63f-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c63f-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c63f-438">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c63f-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c63f-439">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6c63f-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="6c63f-440">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="6c63f-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

