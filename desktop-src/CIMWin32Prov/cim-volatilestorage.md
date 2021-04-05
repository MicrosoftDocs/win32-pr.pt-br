---
description: A \_ classe CIM VolatileStorage representa os recursos e o gerenciamento do armazenamento volátil.
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: Classe CIM_VolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826198"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="e61ab-103">\_Classe CIM VolatileStorage</span><span class="sxs-lookup"><span data-stu-id="e61ab-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="e61ab-104">A classe **CIM \_ VolatileStorage** representa os recursos e o gerenciamento do armazenamento volátil.</span><span class="sxs-lookup"><span data-stu-id="e61ab-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e61ab-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e61ab-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e61ab-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e61ab-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e61ab-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e61ab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e61ab-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e61ab-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61ab-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e61ab-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="e61ab-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e61ab-110">Members</span></span>

<span data-ttu-id="e61ab-111">A classe **CIM \_ VolatileStorage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e61ab-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="e61ab-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e61ab-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e61ab-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e61ab-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e61ab-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="e61ab-114">Methods</span></span>

<span data-ttu-id="e61ab-115">A classe **CIM \_ VolatileStorage** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e61ab-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="e61ab-116">Método</span><span class="sxs-lookup"><span data-stu-id="e61ab-116">Method</span></span>                                                                     | <span data-ttu-id="e61ab-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e61ab-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e61ab-118">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="e61ab-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="e61ab-119">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="e61ab-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e61ab-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e61ab-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e61ab-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="e61ab-122">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e61ab-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e61ab-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e61ab-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e61ab-124">Properties</span></span>

<span data-ttu-id="e61ab-125">A classe **CIM \_ VolatileStorage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e61ab-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e61ab-126">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="e61ab-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-129">Propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="e61ab-129">Read/write properties of the media.</span></span>

<span data-ttu-id="e61ab-130">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-131">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e61ab-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="e61ab-132">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="e61ab-133">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="e61ab-134">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="e61ab-135">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="e61ab-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-137">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e61ab-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="e61ab-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-140">Informações adicionais sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="e61ab-140">Additional error information.</span></span> <span data-ttu-id="e61ab-141">Um exemplo é a verificação de erros e a síndrome de correção (ECC) ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="e61ab-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="e61ab-142">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, o bit exato que falhou poderá ser determinado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="e61ab-143">Esse tipo de dados (síndrome de ECC, dados de verificação de bits ou de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="e61ab-144">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-145">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-146">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="e61ab-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-149">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-150">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-150">Availability and status of the device.</span></span>

<span data-ttu-id="e61ab-151">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e61ab-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e61ab-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-155">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="e61ab-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e61ab-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e61ab-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="e61ab-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e61ab-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="e61ab-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e61ab-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="e61ab-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e61ab-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="e61ab-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e61ab-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="e61ab-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e61ab-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="e61ab-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e61ab-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="e61ab-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e61ab-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="e61ab-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e61ab-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="e61ab-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-166">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e61ab-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="e61ab-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-168">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e61ab-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="e61ab-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-170">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e61ab-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="e61ab-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e61ab-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="e61ab-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-173">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="e61ab-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e61ab-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="e61ab-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-175">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="e61ab-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e61ab-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="e61ab-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-177">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="e61ab-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e61ab-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="e61ab-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-179">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e61ab-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="e61ab-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-181">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="e61ab-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e61ab-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-183">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e61ab-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-185">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-186">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e61ab-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e61ab-187">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="e61ab-188">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), insira um 1 (um).</span><span class="sxs-lookup"><span data-stu-id="e61ab-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="e61ab-189">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e61ab-190">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e61ab-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-191">**Cacheable**</span><span class="sxs-lookup"><span data-stu-id="e61ab-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-192">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e61ab-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-194">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de memória do recurso do sistema DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-195">Se **for true**, essa memória poderá ser armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="e61ab-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="e61ab-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-197">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-199">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de memória do recurso do sistema DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-200">Tipo de cache compatível com a memória.</span><span class="sxs-lookup"><span data-stu-id="e61ab-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="e61ab-201">Se a propriedade **armazenável em cache** estiver definida como **false**, essa propriedade não terá significado e deverá ser definida como 4 ("não aplicável").</span><span class="sxs-lookup"><span data-stu-id="e61ab-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e61ab-202">**Outro** (0)</span><span class="sxs-lookup"><span data-stu-id="e61ab-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-203">**Desconhecido** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="e61ab-204">**Write-back** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="e61ab-205">**Write-through** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e61ab-206">**Não aplicável** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-207">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e61ab-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-210">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e61ab-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-211">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e61ab-211">Short textual description of the object.</span></span>

<span data-ttu-id="e61ab-212">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e61ab-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-214">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e61ab-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-216">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e61ab-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-217">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e61ab-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="e61ab-218">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e61ab-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e61ab-220"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="e61ab-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-221">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e61ab-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e61ab-223">(1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-224">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e61ab-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e61ab-226">(2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e61ab-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e61ab-228">(3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-229">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="e61ab-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e61ab-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e61ab-231">(4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-232">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-232">Device is not working properly.</span></span> <span data-ttu-id="e61ab-233">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e61ab-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e61ab-235">(5)</span><span class="sxs-lookup"><span data-stu-id="e61ab-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-236">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="e61ab-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e61ab-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e61ab-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="e61ab-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-239">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e61ab-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e61ab-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e61ab-241">(7)</span><span class="sxs-lookup"><span data-stu-id="e61ab-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e61ab-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e61ab-243">(8)</span><span class="sxs-lookup"><span data-stu-id="e61ab-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-244">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e61ab-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e61ab-246">(9)</span><span class="sxs-lookup"><span data-stu-id="e61ab-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-247">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-247">Device is not working properly.</span></span> <span data-ttu-id="e61ab-248">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e61ab-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e61ab-250">(10)</span><span class="sxs-lookup"><span data-stu-id="e61ab-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-251">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e61ab-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e61ab-253">(11)</span><span class="sxs-lookup"><span data-stu-id="e61ab-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-254">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e61ab-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e61ab-256">12</span><span class="sxs-lookup"><span data-stu-id="e61ab-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-257">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="e61ab-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e61ab-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e61ab-259">(13)</span><span class="sxs-lookup"><span data-stu-id="e61ab-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-260">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e61ab-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e61ab-262">(14)</span><span class="sxs-lookup"><span data-stu-id="e61ab-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-263">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e61ab-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e61ab-265">(15)</span><span class="sxs-lookup"><span data-stu-id="e61ab-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-266">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="e61ab-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e61ab-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e61ab-268">(16)</span><span class="sxs-lookup"><span data-stu-id="e61ab-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-269">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="e61ab-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e61ab-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e61ab-271">(17)</span><span class="sxs-lookup"><span data-stu-id="e61ab-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-272">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e61ab-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e61ab-274">(18)</span><span class="sxs-lookup"><span data-stu-id="e61ab-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-275">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="e61ab-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e61ab-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e61ab-277">(19)</span><span class="sxs-lookup"><span data-stu-id="e61ab-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e61ab-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e61ab-279">(20)</span><span class="sxs-lookup"><span data-stu-id="e61ab-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-280">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e61ab-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e61ab-282">(21)</span><span class="sxs-lookup"><span data-stu-id="e61ab-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-283">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="e61ab-283">System failure.</span></span> <span data-ttu-id="e61ab-284">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="e61ab-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e61ab-285">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e61ab-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e61ab-287">(22)</span><span class="sxs-lookup"><span data-stu-id="e61ab-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-288">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e61ab-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e61ab-290">(23)</span><span class="sxs-lookup"><span data-stu-id="e61ab-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-291">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="e61ab-291">System failure.</span></span> <span data-ttu-id="e61ab-292">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="e61ab-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e61ab-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e61ab-294">(24)</span><span class="sxs-lookup"><span data-stu-id="e61ab-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-295">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="e61ab-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e61ab-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e61ab-297">(25)</span><span class="sxs-lookup"><span data-stu-id="e61ab-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-298">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e61ab-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e61ab-300">(26)</span><span class="sxs-lookup"><span data-stu-id="e61ab-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-301">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e61ab-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e61ab-303">(27)</span><span class="sxs-lookup"><span data-stu-id="e61ab-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-304">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="e61ab-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e61ab-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e61ab-306">(28)</span><span class="sxs-lookup"><span data-stu-id="e61ab-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-307">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="e61ab-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e61ab-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e61ab-309">(29)</span><span class="sxs-lookup"><span data-stu-id="e61ab-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-310">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-310">Device is disabled.</span></span> <span data-ttu-id="e61ab-311">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="e61ab-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e61ab-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e61ab-313">(30)</span><span class="sxs-lookup"><span data-stu-id="e61ab-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-314">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="e61ab-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e61ab-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e61ab-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e61ab-316">(31)</span><span class="sxs-lookup"><span data-stu-id="e61ab-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-317">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-317">Device is not working properly.</span></span> <span data-ttu-id="e61ab-318">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="e61ab-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e61ab-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-320">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e61ab-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-321">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-322">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e61ab-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-323">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e61ab-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e61ab-324">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-325">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="e61ab-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-326">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e61ab-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-327">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-328">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-329">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="e61ab-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="e61ab-330">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-331">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e61ab-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-335">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e61ab-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-336">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e61ab-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e61ab-337">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e61ab-338">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-339">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e61ab-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-340">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-342">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e61ab-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-343">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e61ab-343">Textual description of the object.</span></span>

<span data-ttu-id="e61ab-344">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e61ab-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-346">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-347">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-348">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e61ab-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-349">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e61ab-350">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-351">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="e61ab-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-352">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e61ab-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-353">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-354">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-355">Endereço final, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para o objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="e61ab-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="e61ab-356">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="e61ab-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="e61ab-357">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e61ab-358">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e61ab-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-359">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="e61ab-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-360">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-362">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,15 "," MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-363">Operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="e61ab-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="e61ab-364">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="e61ab-365">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-366">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e61ab-367">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-368">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="e61ab-369">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="e61ab-370">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="e61ab-371">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="e61ab-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-372">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="e61ab-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-373">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e61ab-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-374">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-375">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-376">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="e61ab-376">Address of the last memory error.</span></span> <span data-ttu-id="e61ab-377">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="e61ab-378">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-379">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e61ab-380">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e61ab-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-381">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e61ab-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-382">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e61ab-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-384">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="e61ab-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e61ab-385">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-386">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="e61ab-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-387">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e61ab-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-389">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="e61ab-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-390">Dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="e61ab-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="e61ab-391">Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="e61ab-392">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-393">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-394">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="e61ab-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-395">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-397">Ordenação de dados armazenados na matriz **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="e61ab-398">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-399">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e61ab-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-401">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="e61ab-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-403">Byte menos significativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="e61ab-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="e61ab-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-405">Byte mais significativo primeiro.</span><span class="sxs-lookup"><span data-stu-id="e61ab-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e61ab-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-407">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-409">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="e61ab-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e61ab-410">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e61ab-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-412">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-414">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="e61ab-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-415">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="e61ab-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="e61ab-416">Os valores 12-14 são indefinidos no esquema CIM, uma vez que a semântica do tipo de erro e se ele foi ou não correto, são misturados no DMI.</span><span class="sxs-lookup"><span data-stu-id="e61ab-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="e61ab-417">A propriedade **CorrectableError** indica se ela foi corrigida.</span><span class="sxs-lookup"><span data-stu-id="e61ab-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="e61ab-418">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e61ab-419">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-420">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e61ab-421">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="e61ab-422">**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="e61ab-423">**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="e61ab-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="e61ab-424">**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="e61ab-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="e61ab-425">**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="e61ab-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="e61ab-426">**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="e61ab-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="e61ab-427">**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="e61ab-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="e61ab-428">**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="e61ab-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="e61ab-429">**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="e61ab-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e61ab-430">**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="e61ab-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e61ab-431">**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="e61ab-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e61ab-432">**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="e61ab-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-433">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="e61ab-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-436">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-437">Cadeia de caracteres de forma livre que descreve o tipo de detecção de erros e correção com suporte na extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e61ab-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="e61ab-438">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-439">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="e61ab-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-440">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e61ab-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-442">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-443">Intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="e61ab-444">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="e61ab-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="e61ab-445">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-446">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e61ab-447">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e61ab-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="e61ab-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-449">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e61ab-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-450">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-451">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="e61ab-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="e61ab-452">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="e61ab-453">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-454">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-455">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="e61ab-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-456">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e61ab-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-458">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-459">Tamanho da transferência de dados em bits que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="e61ab-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="e61ab-460">0 indica que não há erro.</span><span class="sxs-lookup"><span data-stu-id="e61ab-460">0 indicates no error.</span></span> <span data-ttu-id="e61ab-461">Se a propriedade **errorInfo** for igual a 3, "OK", essa propriedade deverá ser definida como 0.</span><span class="sxs-lookup"><span data-stu-id="e61ab-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="e61ab-462">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e61ab-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-464">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e61ab-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-465">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-466">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-467">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-467">Date and time the object was installed.</span></span> <span data-ttu-id="e61ab-468">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e61ab-469">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e61ab-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-471">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e61ab-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-473">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e61ab-474">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-475">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e61ab-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-476">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-478">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e61ab-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-479">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e61ab-479">Label by which the object is known.</span></span> <span data-ttu-id="e61ab-480">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="e61ab-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e61ab-481">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="e61ab-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-483">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e61ab-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-485">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-486">Número total de blocos consecutivos, cada um deles bloqueando o tamanho do valor contido na propriedade **BlockSize** , que formam essa extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e61ab-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="e61ab-487">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e61ab-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="e61ab-488">Se o valor de **BlockSize** for 1 (um), essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e61ab-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="e61ab-489">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e61ab-490">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e61ab-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e61ab-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-492">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-494">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="e61ab-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-495">Cadeia de caracteres de forma livre que fornece informações adicionais se a propriedade **ErrorType** for definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="e61ab-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="e61ab-496">Se um valor diferente de 1 (um), essa cadeia de caracteres não tem significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="e61ab-497">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e61ab-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-501">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e61ab-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-502">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e61ab-503">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e61ab-504">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e61ab-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e61ab-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-506">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-508">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e61ab-509">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="e61ab-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e61ab-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e61ab-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e61ab-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e61ab-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-514">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e61ab-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e61ab-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-516">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="e61ab-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e61ab-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="e61ab-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-518">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="e61ab-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e61ab-519">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e61ab-520">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e61ab-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e61ab-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="e61ab-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-522">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="e61ab-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e61ab-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="e61ab-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e61ab-524">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="e61ab-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e61ab-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-526">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e61ab-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-527">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-528">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="e61ab-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e61ab-529">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e61ab-530">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="e61ab-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e61ab-531">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="e61ab-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e61ab-532">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-533">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="e61ab-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-534">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-535">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-536">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="e61ab-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="e61ab-537">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="e61ab-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-539">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e61ab-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-540">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-541">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-542">Endereço inicial, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para o objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="e61ab-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="e61ab-543">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="e61ab-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="e61ab-544">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e61ab-545">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e61ab-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-546">**Status**</span><span class="sxs-lookup"><span data-stu-id="e61ab-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-547">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-549">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e61ab-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-550">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e61ab-550">Current status of the object.</span></span> <span data-ttu-id="e61ab-551">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e61ab-552">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e61ab-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e61ab-553">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e61ab-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e61ab-554">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e61ab-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e61ab-555">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e61ab-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-556">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e61ab-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e61ab-557">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e61ab-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e61ab-558">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e61ab-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e61ab-559">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e61ab-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e61ab-560">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e61ab-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e61ab-561">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e61ab-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e61ab-562">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e61ab-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e61ab-563">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e61ab-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e61ab-564">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e61ab-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e61ab-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-566">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e61ab-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-567">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-568">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="e61ab-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-569">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-569">State of the logical device.</span></span> <span data-ttu-id="e61ab-570">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e61ab-571">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e61ab-572">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e61ab-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e61ab-573">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e61ab-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e61ab-574">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e61ab-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e61ab-575">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="e61ab-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e61ab-576">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="e61ab-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e61ab-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e61ab-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-578">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-579">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-580">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e61ab-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-581">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="e61ab-582">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="e61ab-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-584">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e61ab-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-585">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-586">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema; Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="e61ab-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="e61ab-587">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e61ab-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e61ab-588">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e61ab-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e61ab-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e61ab-590">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e61ab-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-591">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e61ab-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e61ab-592">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e61ab-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e61ab-593">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e61ab-593">Scoping system's name.</span></span>

<span data-ttu-id="e61ab-594">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e61ab-595">Comentários</span><span class="sxs-lookup"><span data-stu-id="e61ab-595">Remarks</span></span>

<span data-ttu-id="e61ab-596">A classe **CIM \_ VolatileStorage** é derivada da [**\_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e61ab-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e61ab-597">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e61ab-597">WMI does not implement this class.</span></span>

<span data-ttu-id="e61ab-598">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e61ab-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e61ab-599">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e61ab-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e61ab-600">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61ab-600">Requirements</span></span>



| <span data-ttu-id="e61ab-601">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61ab-601">Requirement</span></span> | <span data-ttu-id="e61ab-602">Valor</span><span class="sxs-lookup"><span data-stu-id="e61ab-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e61ab-603">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61ab-603">Minimum supported client</span></span><br/> | <span data-ttu-id="e61ab-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e61ab-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e61ab-605">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61ab-605">Minimum supported server</span></span><br/> | <span data-ttu-id="e61ab-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e61ab-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e61ab-607">Namespace</span><span class="sxs-lookup"><span data-stu-id="e61ab-607">Namespace</span></span><br/>                | <span data-ttu-id="e61ab-608">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e61ab-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e61ab-609">MOF</span><span class="sxs-lookup"><span data-stu-id="e61ab-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e61ab-610"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e61ab-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e61ab-611">DLL</span><span class="sxs-lookup"><span data-stu-id="e61ab-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e61ab-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e61ab-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61ab-613">Confira também</span><span class="sxs-lookup"><span data-stu-id="e61ab-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61ab-614">**\_Memória CIM**</span><span class="sxs-lookup"><span data-stu-id="e61ab-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

