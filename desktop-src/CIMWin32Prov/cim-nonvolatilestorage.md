---
description: A \_ classe CIM NonVolatileStorage representa os recursos e o gerenciamento do armazenamento não volátil. A memória não volátil inclui, nativamente, o armazenamento flash e ROM.
ms.assetid: 39158b31-31f7-460c-aef1-1ca423badad6
ms.tgt_platform: multiple
title: Classe CIM_NonVolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NonVolatileStorage
- CIM_NonVolatileStorage.Access
- CIM_NonVolatileStorage.AdditionalErrorData
- CIM_NonVolatileStorage.Availability
- CIM_NonVolatileStorage.BlockSize
- CIM_NonVolatileStorage.Caption
- CIM_NonVolatileStorage.ConfigManagerErrorCode
- CIM_NonVolatileStorage.ConfigManagerUserConfig
- CIM_NonVolatileStorage.CorrectableError
- CIM_NonVolatileStorage.CreationClassName
- CIM_NonVolatileStorage.Description
- CIM_NonVolatileStorage.DeviceID
- CIM_NonVolatileStorage.EndingAddress
- CIM_NonVolatileStorage.ErrorAccess
- CIM_NonVolatileStorage.ErrorAddress
- CIM_NonVolatileStorage.ErrorCleared
- CIM_NonVolatileStorage.ErrorData
- CIM_NonVolatileStorage.ErrorDataOrder
- CIM_NonVolatileStorage.ErrorDescription
- CIM_NonVolatileStorage.ErrorInfo
- CIM_NonVolatileStorage.ErrorMethodology
- CIM_NonVolatileStorage.ErrorResolution
- CIM_NonVolatileStorage.ErrorTime
- CIM_NonVolatileStorage.ErrorTransferSize
- CIM_NonVolatileStorage.InstallDate
- CIM_NonVolatileStorage.IsWriteable
- CIM_NonVolatileStorage.LastErrorCode
- CIM_NonVolatileStorage.Name
- CIM_NonVolatileStorage.NumberOfBlocks
- CIM_NonVolatileStorage.OtherErrorDescription
- CIM_NonVolatileStorage.PNPDeviceID
- CIM_NonVolatileStorage.PowerManagementCapabilities
- CIM_NonVolatileStorage.PowerManagementSupported
- CIM_NonVolatileStorage.Purpose
- CIM_NonVolatileStorage.StartingAddress
- CIM_NonVolatileStorage.Status
- CIM_NonVolatileStorage.StatusInfo
- CIM_NonVolatileStorage.SystemCreationClassName
- CIM_NonVolatileStorage.SystemLevelAddress
- CIM_NonVolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fca29f0b279994dc0b844127fd1925850094da8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826208"
---
# <a name="cim_nonvolatilestorage-class"></a><span data-ttu-id="e50cc-104">\_Classe CIM NonVolatileStorage</span><span class="sxs-lookup"><span data-stu-id="e50cc-104">CIM\_NonVolatileStorage class</span></span>

<span data-ttu-id="e50cc-105">A classe **CIM \_ NonVolatileStorage** representa os recursos e o gerenciamento do armazenamento não volátil.</span><span class="sxs-lookup"><span data-stu-id="e50cc-105">The **CIM\_NonVolatileStorage** class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="e50cc-106">A memória não volátil inclui, nativamente, o armazenamento flash e ROM.</span><span class="sxs-lookup"><span data-stu-id="e50cc-106">Nonvolatile memory natively includes flash and ROM storage.</span></span> <span data-ttu-id="e50cc-107">Além disso, a memória não volátil pode ser baseada no armazenamento volátil, se a memória volátil tiver suporte de uma bateria.</span><span class="sxs-lookup"><span data-stu-id="e50cc-107">In addition, nonvolatile memory can be based on volatile storage, if the volatile memory is backed by a battery.</span></span> <span data-ttu-id="e50cc-108">Por exemplo, esse cenário seria descrito por uma instância da relação [**\_ AssociatedBattery do CIM**](cim-associatedbattery.md) que faz referência ao armazenamento não volátil como o **dependente** e a bateria como o **antecessor**; e uma instância da relação [**\_ com base em CIM**](cim-basedon.md) que faz referência ao armazenamento não volátil como o armazenamento **dependente** e o volátil como o **antecessor**.</span><span class="sxs-lookup"><span data-stu-id="e50cc-108">For example, this scenario would be described by an instance of the [**CIM\_AssociatedBattery**](cim-associatedbattery.md) relationship that references the nonvolatile storage as the **Dependent** and the battery as the **Antecedent**; and an instance of the [**CIM\_BasedOn**](cim-basedon.md) relationship that references the non-volatile storage as the **Dependent** and the volatile storage as the **Antecedent**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e50cc-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e50cc-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e50cc-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e50cc-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e50cc-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e50cc-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e50cc-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e50cc-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e50cc-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e50cc-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{18074AFA-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_NonVolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
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
  boolean  IsWriteable;
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

## <a name="members"></a><span data-ttu-id="e50cc-114">Membros</span><span class="sxs-lookup"><span data-stu-id="e50cc-114">Members</span></span>

<span data-ttu-id="e50cc-115">A classe **CIM \_ NonVolatileStorage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e50cc-115">The **CIM\_NonVolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="e50cc-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="e50cc-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="e50cc-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e50cc-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e50cc-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="e50cc-118">Methods</span></span>

<span data-ttu-id="e50cc-119">A classe **CIM \_ NonVolatileStorage** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e50cc-119">The **CIM\_NonVolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="e50cc-120">Método</span><span class="sxs-lookup"><span data-stu-id="e50cc-120">Method</span></span>                                                                        | <span data-ttu-id="e50cc-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e50cc-121">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e50cc-122">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="e50cc-122">**Reset**</span></span>](reset-method-in-class-cim-nonvolatilestorage.md)                 | <span data-ttu-id="e50cc-123">Solicita uma redefinição do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="e50cc-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e50cc-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e50cc-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e50cc-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-nonvolatilestorage.md) | <span data-ttu-id="e50cc-126">Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e50cc-127">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="e50cc-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e50cc-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e50cc-128">Properties</span></span>

<span data-ttu-id="e50cc-129">A classe **CIM \_ NonVolatileStorage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e50cc-129">The **CIM\_NonVolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e50cc-130">**Acesso**</span><span class="sxs-lookup"><span data-stu-id="e50cc-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-133">Propriedades de leitura/gravação da mídia.</span><span class="sxs-lookup"><span data-stu-id="e50cc-133">Read/write properties of the media.</span></span>

<span data-ttu-id="e50cc-134">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-135">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e50cc-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="e50cc-136">**Legível** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="e50cc-137">**Gravável** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="e50cc-138">**Suporte de leitura/gravação** (3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="e50cc-139">**Gravar uma vez** (4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="e50cc-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-141">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e50cc-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="e50cc-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-144">Matriz de octetos que contém informações de erro adicionais.</span><span class="sxs-lookup"><span data-stu-id="e50cc-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="e50cc-145">Um exemplo é a verificação de erros e a síndrome de correção (ECC) ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada.</span><span class="sxs-lookup"><span data-stu-id="e50cc-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="e50cc-146">No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, o bit exato que falhou poderá ser determinado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="e50cc-147">Esse tipo de dados (síndrome de ECC, dados de verificação de bits ou de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="e50cc-148">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-149">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-150">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="e50cc-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-151">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-153">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-154">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-154">Availability and status of the device.</span></span>

<span data-ttu-id="e50cc-155">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-155">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e50cc-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-157"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e50cc-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-158"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e50cc-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-159"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e50cc-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="e50cc-160"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e50cc-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="e50cc-161"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e50cc-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="e50cc-162"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e50cc-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="e50cc-163"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e50cc-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="e50cc-164"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e50cc-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="e50cc-165"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e50cc-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="e50cc-166"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e50cc-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="e50cc-167"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e50cc-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="e50cc-168"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-169">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-169">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e50cc-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="e50cc-170"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-171">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-171">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e50cc-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="e50cc-172"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-173">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-173">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e50cc-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="e50cc-174"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e50cc-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="e50cc-175"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-176">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="e50cc-176">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e50cc-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="e50cc-177"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-178">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="e50cc-178">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e50cc-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="e50cc-179"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-180">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="e50cc-180">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e50cc-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="e50cc-181"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-182">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-182">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e50cc-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="e50cc-183"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-184">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="e50cc-184">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-185">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e50cc-185">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-186">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e50cc-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-188">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-189">Tamanho, em bytes, dos blocos que formam a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e50cc-189">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e50cc-190">Se o tamanho do bloco variável, o tamanho máximo do bloco, em bytes, deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-190">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="e50cc-191">Se o tamanho do bloco for desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensões de agregação, memória ou discos lógicos), digite 1 (um).</span><span class="sxs-lookup"><span data-stu-id="e50cc-191">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter 1 (one).</span></span>

<span data-ttu-id="e50cc-192">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-192">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e50cc-193">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e50cc-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-194">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e50cc-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-197">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e50cc-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-198">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e50cc-198">Short textual description of the object.</span></span>

<span data-ttu-id="e50cc-199">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-200">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e50cc-200">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e50cc-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-203">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e50cc-203">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-204">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e50cc-204">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="e50cc-205">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-205">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e50cc-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-206"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e50cc-207"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="e50cc-207">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-208">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-208">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e50cc-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-209"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e50cc-210">(1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-210">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-211">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-211">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e50cc-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-212"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e50cc-213">(2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-213">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e50cc-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-214"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e50cc-215">(3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-215">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-216">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="e50cc-216">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e50cc-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-217"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e50cc-218">(4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-218">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-219">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-219">Device is not working properly.</span></span> <span data-ttu-id="e50cc-220">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-220">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e50cc-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-221"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e50cc-222">(5)</span><span class="sxs-lookup"><span data-stu-id="e50cc-222">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-223">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="e50cc-223">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e50cc-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-224"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e50cc-225"> (6)</span><span class="sxs-lookup"><span data-stu-id="e50cc-225">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-226">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e50cc-226">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e50cc-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-227"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e50cc-228">(7)</span><span class="sxs-lookup"><span data-stu-id="e50cc-228">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e50cc-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-229"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e50cc-230">(8)</span><span class="sxs-lookup"><span data-stu-id="e50cc-230">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-231">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-231">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e50cc-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-232"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e50cc-233">(9)</span><span class="sxs-lookup"><span data-stu-id="e50cc-233">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-234">O dispositivo não está funcionando corretamente; o firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-234">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e50cc-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-235"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e50cc-236">(10)</span><span class="sxs-lookup"><span data-stu-id="e50cc-236">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-237">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-237">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e50cc-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-238"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e50cc-239">(11)</span><span class="sxs-lookup"><span data-stu-id="e50cc-239">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-240">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-240">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e50cc-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-241"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e50cc-242">12</span><span class="sxs-lookup"><span data-stu-id="e50cc-242">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-243">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="e50cc-243">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e50cc-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-244"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e50cc-245">(13)</span><span class="sxs-lookup"><span data-stu-id="e50cc-245">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-246">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-246">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e50cc-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-247"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e50cc-248">(14)</span><span class="sxs-lookup"><span data-stu-id="e50cc-248">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-249">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-249">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e50cc-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-250"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e50cc-251">(15)</span><span class="sxs-lookup"><span data-stu-id="e50cc-251">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-252">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="e50cc-252">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e50cc-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-253"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e50cc-254">(16)</span><span class="sxs-lookup"><span data-stu-id="e50cc-254">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-255">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="e50cc-255">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e50cc-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-256"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e50cc-257">(17)</span><span class="sxs-lookup"><span data-stu-id="e50cc-257">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-258">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-258">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e50cc-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-259"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e50cc-260">(18)</span><span class="sxs-lookup"><span data-stu-id="e50cc-260">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-261">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="e50cc-261">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e50cc-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-262"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e50cc-263">(19)</span><span class="sxs-lookup"><span data-stu-id="e50cc-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e50cc-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-264"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e50cc-265">(20)</span><span class="sxs-lookup"><span data-stu-id="e50cc-265">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-266">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-266">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e50cc-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e50cc-268">(21)</span><span class="sxs-lookup"><span data-stu-id="e50cc-268">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-269">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="e50cc-269">System failure.</span></span> <span data-ttu-id="e50cc-270">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="e50cc-270">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e50cc-271">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-271">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e50cc-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-272"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e50cc-273">(22)</span><span class="sxs-lookup"><span data-stu-id="e50cc-273">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-274">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-274">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e50cc-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-275"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e50cc-276">(23)</span><span class="sxs-lookup"><span data-stu-id="e50cc-276">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-277">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="e50cc-277">System failure.</span></span> <span data-ttu-id="e50cc-278">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="e50cc-278">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e50cc-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-279"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e50cc-280">(24)</span><span class="sxs-lookup"><span data-stu-id="e50cc-280">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-281">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="e50cc-281">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e50cc-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e50cc-283">(25)</span><span class="sxs-lookup"><span data-stu-id="e50cc-283">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-284">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e50cc-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-285"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e50cc-286">(26)</span><span class="sxs-lookup"><span data-stu-id="e50cc-286">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-287">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-287">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e50cc-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-288"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e50cc-289">(27)</span><span class="sxs-lookup"><span data-stu-id="e50cc-289">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-290">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="e50cc-290">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e50cc-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-291"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e50cc-292">(28)</span><span class="sxs-lookup"><span data-stu-id="e50cc-292">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-293">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="e50cc-293">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e50cc-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-294"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e50cc-295">(29)</span><span class="sxs-lookup"><span data-stu-id="e50cc-295">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-296">O dispositivo está desabilitado; o firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="e50cc-296">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e50cc-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e50cc-298">(30)</span><span class="sxs-lookup"><span data-stu-id="e50cc-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-299">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="e50cc-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e50cc-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="e50cc-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e50cc-301">(31)</span><span class="sxs-lookup"><span data-stu-id="e50cc-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-302">O dispositivo não está funcionando corretamente; O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="e50cc-302">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e50cc-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-304">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e50cc-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-306">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e50cc-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-307">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e50cc-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e50cc-308">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-309">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="e50cc-309">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-310">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e50cc-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-312">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-313">Se **for true**, o erro mais recente era corrigível.</span><span class="sxs-lookup"><span data-stu-id="e50cc-313">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="e50cc-314">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-314">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-315">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-315">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e50cc-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-317">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-318">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-319">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e50cc-319">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-320">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="e50cc-320">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e50cc-321">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-321">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e50cc-322">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-323">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e50cc-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-326">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e50cc-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-327">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e50cc-327">Textual description of the object.</span></span>

<span data-ttu-id="e50cc-328">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-329">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e50cc-329">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-332">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e50cc-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-333">Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-333">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e50cc-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-335">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="e50cc-335">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-336">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e50cc-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-338">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,4 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-339">Endereço final, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para o objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="e50cc-339">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="e50cc-340">O endereço final é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="e50cc-340">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="e50cc-341">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e50cc-342">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e50cc-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-343">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="e50cc-343">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-344">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-345">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-346">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,15 "," MIF. \|Matriz de memória física da DMTF \| 1,10 ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-347">Enumeração que indica a operação de acesso à memória que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="e50cc-347">Enumeration that indicates the memory access operation that caused the last error.</span></span> <span data-ttu-id="e50cc-348">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-348">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="e50cc-349">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-349">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-350">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-350">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e50cc-351">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-351">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-352">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-352">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="e50cc-353">**Leitura** (3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-353">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="e50cc-354">**Gravação** (4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-354">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="e50cc-355">**Gravação parcial** (5)</span><span class="sxs-lookup"><span data-stu-id="e50cc-355">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-356">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="e50cc-356">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-357">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e50cc-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-359">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-360">Endereço do último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="e50cc-360">Address of the last memory error.</span></span> <span data-ttu-id="e50cc-361">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-361">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="e50cc-362">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-362">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-363">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-363">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e50cc-364">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e50cc-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e50cc-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-366">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e50cc-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-367">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-368">Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.</span><span class="sxs-lookup"><span data-stu-id="e50cc-368">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e50cc-369">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="e50cc-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-371">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e50cc-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-373">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)</span><span class="sxs-lookup"><span data-stu-id="e50cc-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-374">Dados capturados durante o último acesso de memória incorreto.</span><span class="sxs-lookup"><span data-stu-id="e50cc-374">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="e50cc-375">Os dados ocupam os primeiros *n* octetos da matriz que são necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-375">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="e50cc-376">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-376">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-377">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-377">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="e50cc-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-379">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-380">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-381">Ordenação de dados armazenados na propriedade **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-381">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="e50cc-382">Se **ErrorTransferSize** for 0, essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-382">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-383">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-383">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-384">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e50cc-384">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="e50cc-385">**Byte menos significativo primeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-385">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="e50cc-386">**Byte mais significativo primeiro** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-386">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-387">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e50cc-387">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-390">Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="e50cc-390">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e50cc-391">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-392">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="e50cc-392">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-393">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-395">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="e50cc-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-396">Tipo de erro que ocorreu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="e50cc-396">Type of error that occurred most recently.</span></span> <span data-ttu-id="e50cc-397">Os valores de 12 a 14 são indefinidos no esquema CIM porque a DMI combina a semântica do tipo de erro e se ela foi corrigida.</span><span class="sxs-lookup"><span data-stu-id="e50cc-397">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="e50cc-398">Se um erro é corrigível é indicado na propriedade **CorrectableError** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-398">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span> <span data-ttu-id="e50cc-399">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e50cc-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-400"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-401">Outros.</span><span class="sxs-lookup"><span data-stu-id="e50cc-401">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-403">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-403">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e50cc-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-404"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-405">OK.</span><span class="sxs-lookup"><span data-stu-id="e50cc-405">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="e50cc-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Leitura inadequada** (4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-406"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-407">Leitura inadequada.</span><span class="sxs-lookup"><span data-stu-id="e50cc-407">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="e50cc-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Erro de paridade** (5)</span><span class="sxs-lookup"><span data-stu-id="e50cc-408"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-409">Erro de paridade.</span><span class="sxs-lookup"><span data-stu-id="e50cc-409">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="e50cc-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Erro de bit único** (6)</span><span class="sxs-lookup"><span data-stu-id="e50cc-410"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-411">Erro de bit único.</span><span class="sxs-lookup"><span data-stu-id="e50cc-411">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="e50cc-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Erro de bit duplo** (7)</span><span class="sxs-lookup"><span data-stu-id="e50cc-412"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-413">Erro de bit duplo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-413">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="e50cc-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Erro de vários bits** (8)</span><span class="sxs-lookup"><span data-stu-id="e50cc-414"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-415">Erro de vários bits.</span><span class="sxs-lookup"><span data-stu-id="e50cc-415">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="e50cc-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Erro de Nibble** (9)</span><span class="sxs-lookup"><span data-stu-id="e50cc-416"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-417">Erro de Nibble.</span><span class="sxs-lookup"><span data-stu-id="e50cc-417">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="e50cc-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Erro de soma de verificação** (10)</span><span class="sxs-lookup"><span data-stu-id="e50cc-418"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-419">Erro de soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="e50cc-419">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="e50cc-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Erro de CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="e50cc-420"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-421">Erro de CRC.</span><span class="sxs-lookup"><span data-stu-id="e50cc-421">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e50cc-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (12)</span><span class="sxs-lookup"><span data-stu-id="e50cc-422"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-423">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-423">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e50cc-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (13)</span><span class="sxs-lookup"><span data-stu-id="e50cc-424"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-425">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-425">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="e50cc-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Indefinido** (14)</span><span class="sxs-lookup"><span data-stu-id="e50cc-426"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-427">Indefinido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-427">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-428">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="e50cc-428">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-429">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-430">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-431">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-431">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-432">Especifica se algoritmos de paridade, algoritmos de CRC, ECC ou outros mecanismos são usados.</span><span class="sxs-lookup"><span data-stu-id="e50cc-432">Specifies whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used.</span></span> <span data-ttu-id="e50cc-433">Também é possível fornecer detalhes sobre o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-433">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="e50cc-434">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-434">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-435">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="e50cc-435">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-436">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e50cc-436">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-438">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-439">Intervalo, em bytes, para o qual o último erro pode ser resolvido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-439">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="e50cc-440">Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000.</span><span class="sxs-lookup"><span data-stu-id="e50cc-440">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="e50cc-441">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-441">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-442">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e50cc-443">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e50cc-443">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-444">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="e50cc-444">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-445">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e50cc-445">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-447">Hora em que ocorreu o último erro de memória.</span><span class="sxs-lookup"><span data-stu-id="e50cc-447">Time that the last memory error occurred.</span></span> <span data-ttu-id="e50cc-448">O tipo de erro é descrito pela propriedade **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-448">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="e50cc-449">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-449">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-450">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-450">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-451">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="e50cc-451">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-452">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e50cc-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-454">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-455">Tamanho da transferência de dados, em bits, que causou o último erro.</span><span class="sxs-lookup"><span data-stu-id="e50cc-455">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="e50cc-456">Um valor de 0 (zero) não indica nenhum erro.</span><span class="sxs-lookup"><span data-stu-id="e50cc-456">A value of 0 (zero) indicates no error.</span></span> <span data-ttu-id="e50cc-457">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e50cc-457">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="e50cc-458">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e50cc-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-460">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e50cc-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-461">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-462">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-463">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-463">Date and time the object was installed.</span></span> <span data-ttu-id="e50cc-464">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-464">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e50cc-465">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-466">**IsWriteable**</span><span class="sxs-lookup"><span data-stu-id="e50cc-466">**IsWriteable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-467">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e50cc-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-468">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-469">Se for **true**, o armazenamento não volátil será gravável.</span><span class="sxs-lookup"><span data-stu-id="e50cc-469">If **TRUE**, non-volatile storage is writeable.</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e50cc-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-471">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e50cc-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-473">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e50cc-474">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-475">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e50cc-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-476">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-477">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-478">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e50cc-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-479">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e50cc-479">Label by which the object is known.</span></span> <span data-ttu-id="e50cc-480">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="e50cc-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e50cc-481">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="e50cc-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-483">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e50cc-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-484">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-485">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-486">Número total de blocos consecutivos, cada bloco é o tamanho do valor contido na propriedade **BlockSize** , que forma a extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e50cc-486">Total number of consecutive blocks, each block is the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="e50cc-487">O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e50cc-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="e50cc-488">Se o valor de **BlockSize** for 1 (um), essa propriedade será o tamanho total da extensão de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e50cc-488">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="e50cc-489">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e50cc-490">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e50cc-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e50cc-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-492">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-493">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-494">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="e50cc-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-495">Cadeia de caracteres de forma livre que fornece informações se a propriedade **ErrorType** estiver definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="e50cc-495">Free-form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="e50cc-496">Se não estiver definido como 1, essa cadeia de caracteres não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-496">If not set to 1, this string has no meaning.</span></span>

<span data-ttu-id="e50cc-497">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e50cc-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-499">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-500">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-501">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e50cc-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-502">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e50cc-503">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e50cc-504">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e50cc-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e50cc-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-506">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-508">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e50cc-509">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="e50cc-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e50cc-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e50cc-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e50cc-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e50cc-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-514">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e50cc-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e50cc-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-516">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="e50cc-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e50cc-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="e50cc-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-518">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="e50cc-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e50cc-519">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e50cc-520">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e50cc-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e50cc-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="e50cc-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-522">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="e50cc-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e50cc-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="e50cc-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e50cc-524">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="e50cc-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e50cc-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-526">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e50cc-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-527">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-528">Se for **true**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="e50cc-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e50cc-529">Se **for false**, o valor inteiro 1 ("sem suporte") deverá ser a única entrada na matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e50cc-530">Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou se estão habilitados, quais recursos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="e50cc-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e50cc-531">Para obter mais informações, consulte a matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="e50cc-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e50cc-532">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-533">**Finalidade**</span><span class="sxs-lookup"><span data-stu-id="e50cc-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-534">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-535">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-536">Cadeia de caracteres de forma livre que descreve a mídia e seu uso.</span><span class="sxs-lookup"><span data-stu-id="e50cc-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="e50cc-537">Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="e50cc-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-539">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e50cc-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-540">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-541">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Os \| endereços mapeados da matriz de memória DMTF \| 1,3 "," MIF. \|Endereços mapeados do dispositivo \| de memória DMTF 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-542">Endereço inicial referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória para esse objeto de memória.</span><span class="sxs-lookup"><span data-stu-id="e50cc-542">Beginning address that is referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="e50cc-543">O endereço inicial é especificado em kilobytes.</span><span class="sxs-lookup"><span data-stu-id="e50cc-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="e50cc-544">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e50cc-545">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e50cc-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-546">**Status**</span><span class="sxs-lookup"><span data-stu-id="e50cc-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-547">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-548">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-549">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e50cc-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-550">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e50cc-550">Current status of the object.</span></span>

<span data-ttu-id="e50cc-551">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e50cc-552">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e50cc-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e50cc-553">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e50cc-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e50cc-554">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e50cc-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e50cc-555">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e50cc-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-556">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e50cc-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e50cc-557">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e50cc-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e50cc-558">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e50cc-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e50cc-559">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e50cc-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e50cc-560">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e50cc-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e50cc-561">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e50cc-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e50cc-562">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e50cc-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e50cc-563">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e50cc-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e50cc-564">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e50cc-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e50cc-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-566">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e50cc-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-567">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-568">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="e50cc-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-569">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-569">State of the logical device.</span></span> <span data-ttu-id="e50cc-570">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e50cc-571">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e50cc-572">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="e50cc-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e50cc-573">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="e50cc-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e50cc-574">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e50cc-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e50cc-575">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="e50cc-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e50cc-576">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="e50cc-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e50cc-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e50cc-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-578">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-579">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-580">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e50cc-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-581">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="e50cc-582">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="e50cc-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-584">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e50cc-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-585">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-586">Se **for true**, as informações de endereço na propriedade **ErrorAddress** serão um endereço de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="e50cc-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="e50cc-587">Se for **false**, será um endereço físico.</span><span class="sxs-lookup"><span data-stu-id="e50cc-587">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="e50cc-588">Se a propriedade **errorInfo** for igual a 3 ("OK"), essa propriedade não terá significado.</span><span class="sxs-lookup"><span data-stu-id="e50cc-588">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="e50cc-589">Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-589">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e50cc-590">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e50cc-590">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e50cc-591">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e50cc-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-592">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e50cc-592">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e50cc-593">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e50cc-593">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e50cc-594">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="e50cc-594">Scoping system's name.</span></span>

<span data-ttu-id="e50cc-595">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-595">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e50cc-596">Comentários</span><span class="sxs-lookup"><span data-stu-id="e50cc-596">Remarks</span></span>

<span data-ttu-id="e50cc-597">A classe **CIM \_ NonVolatileStorage** é derivada da [**\_ memória CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="e50cc-597">The **CIM\_NonVolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="e50cc-598">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e50cc-598">WMI does not implement this class.</span></span>

<span data-ttu-id="e50cc-599">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e50cc-599">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e50cc-600">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e50cc-600">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e50cc-601">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e50cc-601">Requirements</span></span>



| <span data-ttu-id="e50cc-602">Requisito</span><span class="sxs-lookup"><span data-stu-id="e50cc-602">Requirement</span></span> | <span data-ttu-id="e50cc-603">Valor</span><span class="sxs-lookup"><span data-stu-id="e50cc-603">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e50cc-604">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e50cc-604">Minimum supported client</span></span><br/> | <span data-ttu-id="e50cc-605">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e50cc-605">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e50cc-606">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e50cc-606">Minimum supported server</span></span><br/> | <span data-ttu-id="e50cc-607">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e50cc-607">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e50cc-608">Namespace</span><span class="sxs-lookup"><span data-stu-id="e50cc-608">Namespace</span></span><br/>                | <span data-ttu-id="e50cc-609">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e50cc-609">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e50cc-610">MOF</span><span class="sxs-lookup"><span data-stu-id="e50cc-610">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e50cc-611"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e50cc-611"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e50cc-612">DLL</span><span class="sxs-lookup"><span data-stu-id="e50cc-612">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e50cc-613"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e50cc-613"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e50cc-614">Confira também</span><span class="sxs-lookup"><span data-stu-id="e50cc-614">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50cc-615">**\_Memória CIM**</span><span class="sxs-lookup"><span data-stu-id="e50cc-615">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

