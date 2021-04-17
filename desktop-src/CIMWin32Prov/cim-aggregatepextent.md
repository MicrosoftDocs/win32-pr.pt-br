---
description: A \_ classe CIM AggregatePExtent fornece informações resumidas sobre blocos lógicos endereçáveis, que estão no mesmo grupo de redundância de armazenamento e localizados na mesma mídia física.
ms.assetid: c8def347-e8d7-48d5-94d0-f6e704e7b40e
ms.tgt_platform: multiple
title: Classe CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent
- CIM_AggregatePExtent.Caption
- CIM_AggregatePExtent.Description
- CIM_AggregatePExtent.InstallDate
- CIM_AggregatePExtent.Name
- CIM_AggregatePExtent.Status
- CIM_AggregatePExtent.Availability
- CIM_AggregatePExtent.ConfigManagerErrorCode
- CIM_AggregatePExtent.ConfigManagerUserConfig
- CIM_AggregatePExtent.CreationClassName
- CIM_AggregatePExtent.DeviceID
- CIM_AggregatePExtent.PowerManagementCapabilities
- CIM_AggregatePExtent.ErrorCleared
- CIM_AggregatePExtent.ErrorDescription
- CIM_AggregatePExtent.LastErrorCode
- CIM_AggregatePExtent.PNPDeviceID
- CIM_AggregatePExtent.PowerManagementSupported
- CIM_AggregatePExtent.StatusInfo
- CIM_AggregatePExtent.SystemCreationClassName
- CIM_AggregatePExtent.SystemName
- CIM_AggregatePExtent.Access
- CIM_AggregatePExtent.BlockSize
- CIM_AggregatePExtent.ErrorMethodology
- CIM_AggregatePExtent.Purpose
- CIM_AggregatePExtent.NumberOfBlocks
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2f1b2b5b7e08876317888d02d4830cd72659bc0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501013"
---
# <a name="cim_aggregatepextent-class"></a><span data-ttu-id="c859f-103">\_Classe CIM AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="c859f-103">CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="c859f-104">A classe **CIM \_ AggregatePExtent** fornece informações resumidas sobre blocos lógicos endereçáveis, que estão no mesmo grupo de redundância de armazenamento e localizados na mesma mídia física.</span><span class="sxs-lookup"><span data-stu-id="c859f-104">The **CIM\_AggregatePExtent** class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

<span data-ttu-id="c859f-105">A classe **CIM \_ AggregatePExtent** é um agrupamento alternativo para extensões físicas quando apenas informações resumidas são necessárias ou quando a configuração automática é usada.</span><span class="sxs-lookup"><span data-stu-id="c859f-105">The **CIM\_AggregatePExtent** class is an alternative grouping for physical extents when only summary information is needed, or when automatic configuration is used.</span></span> <span data-ttu-id="c859f-106">A configuração automática pode resultar em milhares de extensões físicas sendo definidas.</span><span class="sxs-lookup"><span data-stu-id="c859f-106">Automatic configuration can result in thousands of physical extents being defined.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c859f-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c859f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c859f-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c859f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c859f-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c859f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c859f-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c859f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c859f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c859f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979F-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AggregatePExtent : CIM_StorageExtent
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
  string   Purpose;
  uint64   NumberOfBlocks;
};
```

## <a name="members"></a><span data-ttu-id="c859f-112">Membros</span><span class="sxs-lookup"><span data-stu-id="c859f-112">Members</span></span>

<span data-ttu-id="c859f-113">A classe **CIM \_ AggregatePExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c859f-113">The **CIM\_AggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="c859f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c859f-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c859f-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c859f-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c859f-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="c859f-116">Methods</span></span>

<span data-ttu-id="c859f-117">A classe **CIM \_ AggregatePExtent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c859f-117">The **CIM\_AggregatePExtent** class has these methods.</span></span>



| <span data-ttu-id="c859f-118">Método</span><span class="sxs-lookup"><span data-stu-id="c859f-118">Method</span></span>                                                                      | <span data-ttu-id="c859f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c859f-119">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c859f-120">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="c859f-120">**Reset**</span></span>](reset-method-in-class-cim-aggregatepextent.md)                 | <span data-ttu-id="c859f-121">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c859f-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="c859f-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c859f-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="c859f-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c859f-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md) | <span data-ttu-id="c859f-124">Define o estado de energia desejado para um dispositivo lógico e quando o dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="c859f-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="c859f-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c859f-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c859f-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c859f-126">Properties</span></span>

<span data-ttu-id="c859f-127">A classe **CIM \_ AggregatePExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c859f-127">The **CIM\_AggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c859f-128">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="c859f-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c859f-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-131">Descreve as propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="c859f-131">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="c859f-132">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c859f-133">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c859f-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c859f-134">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="c859f-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c859f-135">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="c859f-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c859f-136">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="c859f-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c859f-137">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="c859f-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c859f-138">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="c859f-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-139">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c859f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-141">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c859f-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-142">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c859f-142">Availability and status of the device.</span></span>

<span data-ttu-id="c859f-143">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c859f-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c859f-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c859f-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c859f-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c859f-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c859f-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c859f-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="c859f-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c859f-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="c859f-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c859f-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="c859f-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c859f-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="c859f-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c859f-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="c859f-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c859f-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="c859f-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c859f-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c859f-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c859f-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c859f-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c859f-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="c859f-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c859f-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="c859f-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-157">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c859f-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c859f-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="c859f-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-159">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="c859f-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c859f-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c859f-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-161">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="c859f-161">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c859f-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="c859f-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c859f-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="c859f-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-164">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c859f-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c859f-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c859f-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-166">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c859f-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c859f-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="c859f-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-168">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="c859f-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c859f-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c859f-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-170">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="c859f-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c859f-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="c859f-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-172">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="c859f-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c859f-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c859f-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-174">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c859f-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-176">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="c859f-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-177">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c859f-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="c859f-178">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c859f-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="c859f-179">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="c859f-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="c859f-180">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c859f-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c859f-181">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-182">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c859f-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-185">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c859f-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-186">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c859f-186">A short textual description of the object.</span></span>

<span data-ttu-id="c859f-187">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c859f-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-189">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c859f-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-191">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c859f-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-192">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c859f-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c859f-193">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c859f-194">**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c859f-194">**This device is working properly.**</span></span> <span data-ttu-id="c859f-195"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="c859f-195">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c859f-196">**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="c859f-196">**This device is not configured correctly.**</span></span> <span data-ttu-id="c859f-197">(1)</span><span class="sxs-lookup"><span data-stu-id="c859f-197">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c859f-198">**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-198">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c859f-199">(2)</span><span class="sxs-lookup"><span data-stu-id="c859f-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c859f-200">**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c859f-200">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c859f-201">(3)</span><span class="sxs-lookup"><span data-stu-id="c859f-201">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c859f-202">**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c859f-202">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c859f-203">(4)</span><span class="sxs-lookup"><span data-stu-id="c859f-203">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c859f-204">**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="c859f-204">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c859f-205">(5)</span><span class="sxs-lookup"><span data-stu-id="c859f-205">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c859f-206">**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c859f-206">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c859f-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="c859f-207">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c859f-208">**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c859f-208">**Cannot filter.**</span></span> <span data-ttu-id="c859f-209">(7)</span><span class="sxs-lookup"><span data-stu-id="c859f-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c859f-210">**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="c859f-210">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c859f-211">(8)</span><span class="sxs-lookup"><span data-stu-id="c859f-211">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c859f-212">**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="c859f-212">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c859f-213">(9)</span><span class="sxs-lookup"><span data-stu-id="c859f-213">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c859f-214">**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="c859f-214">**This device cannot start.**</span></span> <span data-ttu-id="c859f-215">(10)</span><span class="sxs-lookup"><span data-stu-id="c859f-215">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c859f-216">**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="c859f-216">**This device failed.**</span></span> <span data-ttu-id="c859f-217">(11)</span><span class="sxs-lookup"><span data-stu-id="c859f-217">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c859f-218">**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="c859f-218">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c859f-219">12</span><span class="sxs-lookup"><span data-stu-id="c859f-219">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c859f-220">**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-220">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c859f-221">(13)</span><span class="sxs-lookup"><span data-stu-id="c859f-221">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c859f-222">**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="c859f-222">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c859f-223">(14)</span><span class="sxs-lookup"><span data-stu-id="c859f-223">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c859f-224">**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="c859f-224">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c859f-225">(15)</span><span class="sxs-lookup"><span data-stu-id="c859f-225">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c859f-226">**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="c859f-226">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c859f-227">(16)</span><span class="sxs-lookup"><span data-stu-id="c859f-227">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c859f-228">**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="c859f-228">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c859f-229">(17)</span><span class="sxs-lookup"><span data-stu-id="c859f-229">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c859f-230">**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-230">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c859f-231">(18)</span><span class="sxs-lookup"><span data-stu-id="c859f-231">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c859f-232">**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="c859f-232">**Failure using the VxD loader.**</span></span> <span data-ttu-id="c859f-233">(19)</span><span class="sxs-lookup"><span data-stu-id="c859f-233">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c859f-234">**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="c859f-234">**Your registry might be corrupted.**</span></span> <span data-ttu-id="c859f-235">(20)</span><span class="sxs-lookup"><span data-stu-id="c859f-235">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c859f-236">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-236">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c859f-237">(21)</span><span class="sxs-lookup"><span data-stu-id="c859f-237">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c859f-238">**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c859f-238">**This device is disabled.**</span></span> <span data-ttu-id="c859f-239">(22)</span><span class="sxs-lookup"><span data-stu-id="c859f-239">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c859f-240">**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="c859f-240">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c859f-241">(23)</span><span class="sxs-lookup"><span data-stu-id="c859f-241">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c859f-242">**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="c859f-242">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c859f-243">(24)</span><span class="sxs-lookup"><span data-stu-id="c859f-243">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c859f-244">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-244">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c859f-245">(25)</span><span class="sxs-lookup"><span data-stu-id="c859f-245">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c859f-246">**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c859f-247">(26)</span><span class="sxs-lookup"><span data-stu-id="c859f-247">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c859f-248">**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="c859f-248">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c859f-249">(27)</span><span class="sxs-lookup"><span data-stu-id="c859f-249">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c859f-250">**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="c859f-250">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c859f-251">(28)</span><span class="sxs-lookup"><span data-stu-id="c859f-251">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c859f-252">**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="c859f-252">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c859f-253">(29)</span><span class="sxs-lookup"><span data-stu-id="c859f-253">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c859f-254">**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c859f-254">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c859f-255">(30)</span><span class="sxs-lookup"><span data-stu-id="c859f-255">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c859f-256">**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c859f-256">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c859f-257">(31)</span><span class="sxs-lookup"><span data-stu-id="c859f-257">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c859f-258">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c859f-258">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-259">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c859f-259">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-261">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c859f-261">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-262">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c859f-262">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c859f-263">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-263">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-264">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c859f-264">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-265">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-267">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c859f-267">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c859f-268">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="c859f-268">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c859f-269">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c859f-269">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c859f-270">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-271">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c859f-271">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-272">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-273">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-274">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c859f-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-275">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c859f-275">A textual description of the object.</span></span>

<span data-ttu-id="c859f-276">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-277">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c859f-277">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-278">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-280">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c859f-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c859f-281">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c859f-281">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c859f-282">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-283">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c859f-283">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-284">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c859f-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-286">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="c859f-286">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c859f-287">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-288">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c859f-288">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-291">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="c859f-291">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c859f-292">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-293">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c859f-293">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-294">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-296">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c859f-296">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="c859f-297">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-297">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c859f-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-299">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c859f-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-301">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c859f-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-302">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c859f-302">Indicates when the object was installed.</span></span> <span data-ttu-id="c859f-303">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="c859f-303">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c859f-304">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-305">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c859f-305">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-306">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c859f-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-307">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-308">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c859f-308">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c859f-309">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-310">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c859f-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-311">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-313">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c859f-313">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-314">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c859f-314">Label by which the object is known.</span></span> <span data-ttu-id="c859f-315">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="c859f-315">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c859f-316">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-317">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c859f-317">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-318">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c859f-318">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-319">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-320">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensão física de agregação DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="c859f-320">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Aggregate Physical Extent\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-321">Número total de blocos (incluindo os blocos de dados de verificação) contidos nessa extensão física agregada.</span><span class="sxs-lookup"><span data-stu-id="c859f-321">Total number of blocks (including the check data blocks) contained in this aggregate physical extent.</span></span> <span data-ttu-id="c859f-322">O tamanho do bloco (uma propriedade herdada) deve ser definido com o mesmo valor do dispositivo de acesso à mídia associado a essa extensão.</span><span class="sxs-lookup"><span data-stu-id="c859f-322">The block size (an inherited property) should be set to the same value as for the media access device associated with this extent.</span></span>

</dd> <dt>

<span data-ttu-id="c859f-323">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c859f-323">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-326">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c859f-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-327">Indica o identificador do dispositivo de Plug and Play do Win32 do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c859f-327">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c859f-328">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c859f-328">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c859f-329">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-330">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c859f-330">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-331">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c859f-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c859f-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-333">Indica os recursos específicos relacionados à energia do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c859f-333">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c859f-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c859f-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c859f-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-336">As capacidades relacionadas à energia são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="c859f-336">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c859f-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="c859f-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-338">Não há suporte para capacidades relacionadas a energia para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c859f-338">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c859f-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c859f-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-340">As capacidades relacionadas à energia foram desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="c859f-340">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c859f-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c859f-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-342">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c859f-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c859f-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c859f-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-344">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="c859f-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c859f-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="c859f-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-346">Há suporte para o método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="c859f-346">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="c859f-347">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="c859f-347">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="c859f-348">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c859f-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c859f-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="c859f-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-350">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia").</span><span class="sxs-lookup"><span data-stu-id="c859f-350">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c859f-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="c859f-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c859f-352">O método **SetPowerState** pode ser invocado com o parâmetro *PowerState* definido como 5 ("ciclo de energia") e o parâmetro de *hora* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="c859f-352">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c859f-353">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c859f-353">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-354">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c859f-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-355">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-356">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="c859f-356">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c859f-357">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c859f-357">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c859f-358">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="c859f-358">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c859f-359">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c859f-359">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c859f-360">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-361">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="c859f-361">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-362">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c859f-364">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="c859f-364">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="c859f-365">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-365">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-366">**Status**</span><span class="sxs-lookup"><span data-stu-id="c859f-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-369">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c859f-369">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-370">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c859f-370">String that indicates the current status of the object.</span></span> <span data-ttu-id="c859f-371">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="c859f-371">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c859f-372">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="c859f-372">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c859f-373">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="c859f-373">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c859f-374">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c859f-374">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c859f-375">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c859f-375">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c859f-376">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c859f-376">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c859f-377">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c859f-378">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c859f-378">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c859f-379">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c859f-379">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c859f-380">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c859f-380">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c859f-381">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c859f-381">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c859f-382">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c859f-382">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c859f-383">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c859f-383">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c859f-384">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c859f-384">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c859f-385">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c859f-385">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c859f-386">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c859f-386">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c859f-387">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c859f-387">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c859f-388">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c859f-388">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c859f-389">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c859f-389">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c859f-390">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c859f-390">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c859f-391">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c859f-391">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-392">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c859f-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="c859f-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c859f-395">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c859f-395">State of the logical device.</span></span> <span data-ttu-id="c859f-396">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 ("não aplicável") deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="c859f-396">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="c859f-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c859f-398">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c859f-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c859f-399">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="c859f-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c859f-400">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c859f-400">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c859f-401">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c859f-401">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c859f-402">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="c859f-402">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c859f-403">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c859f-403">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-404">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-406">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c859f-406">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c859f-407">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c859f-407">The scoping system's creation class name.</span></span>

<span data-ttu-id="c859f-408">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c859f-409">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c859f-409">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c859f-410">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c859f-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c859f-411">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c859f-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c859f-412">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c859f-412">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c859f-413">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="c859f-413">The scoping system's name.</span></span>

<span data-ttu-id="c859f-414">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c859f-415">Comentários</span><span class="sxs-lookup"><span data-stu-id="c859f-415">Remarks</span></span>

<span data-ttu-id="c859f-416">A classe **CIM \_ AggregatePExtent** é derivada de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="c859f-416">The **CIM\_AggregatePExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="c859f-417">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c859f-417">WMI does not implement this class.</span></span>

<span data-ttu-id="c859f-418">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c859f-418">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c859f-419">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c859f-419">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c859f-420">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c859f-420">Requirements</span></span>



| <span data-ttu-id="c859f-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="c859f-421">Requirement</span></span> | <span data-ttu-id="c859f-422">Valor</span><span class="sxs-lookup"><span data-stu-id="c859f-422">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c859f-423">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c859f-423">Minimum supported client</span></span><br/> | <span data-ttu-id="c859f-424">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c859f-424">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c859f-425">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c859f-425">Minimum supported server</span></span><br/> | <span data-ttu-id="c859f-426">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c859f-426">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c859f-427">Namespace</span><span class="sxs-lookup"><span data-stu-id="c859f-427">Namespace</span></span><br/>                | <span data-ttu-id="c859f-428">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c859f-428">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c859f-429">MOF</span><span class="sxs-lookup"><span data-stu-id="c859f-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c859f-430"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c859f-430"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c859f-431">DLL</span><span class="sxs-lookup"><span data-stu-id="c859f-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c859f-432"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c859f-432"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c859f-433">Confira também</span><span class="sxs-lookup"><span data-stu-id="c859f-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c859f-434">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="c859f-434">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="c859f-435">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="c859f-435">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

